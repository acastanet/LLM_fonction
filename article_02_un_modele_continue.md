---
type: note
slug: un-modele-ne-repond-pas-il-continue
status: copy-edit
title: "Un modèle ne répond pas, il continue"
description: "Du vecteur au prochain token : comment une réponse se construit dans une boucle au lieu d'être rédigée d'un bloc."
image: figure-vecteurs-couches.svg
image_alt: "Des vecteurs traversent les couches ; le dernier état produit des logits, un token est sélectionné puis réinjecté dans la séquence."
series: "Une phrase dans la machine"
part: 2
technical_review: completed
editorial_review: pending
sources_checked: 2026-08-04
---

**Une phrase dans la machine — Partie 2/4.** Dans l'article précédent, une phrase est devenue une suite ordonnée de représentations numériques. Dans celui-ci, nous suivons ces vecteurs à travers le transformeur, jusqu'au prochain token, puis au suivant.

# Un modèle ne répond pas, il continue

*Du vecteur au prochain token*

## Vous écrivez une phrase, le texte se déroule

Vous écrivez une question, vous validez, un texte se déroule. L'impression est immédiate : quelqu'un a lu, conçu une réponse, puis entrepris de l'afficher. Pourtant, le texte peut commencer avant que sa dernière phrase soit déterminée. Personne ne l'a rédigé d'un bloc dans une arrière-salle numérique.

Regardons précisément ce qui se passe. La question « Pourquoi aimons-nous le sucre ? » a déjà été découpée en tokens, indexée et transformée en vecteurs. Ceux-ci traversent maintenant une pile de blocs de transformeur. À la sortie, le système attribue un score à chaque token possible, transforme ces scores en probabilités, puis une procédure retient une continuation. Le nouveau token rejoint la séquence. Le calcul recommence.

Le paradoxe tient dans cette boucle : la réponse donne une impression d'ensemble alors qu'elle est produite une unité après l'autre. Pour le comprendre, il faut suivre non une pensée cachée, mais des positions qui se transforment et échangent de l'information.

![La génération est une boucle](figure-vecteurs-couches.svg)

*Schéma de principe d'un transformeur génératif. L'attention causale, la projection et la sélection sont simplifiées ; le cache utilisé en production n'est pas représenté.*

## Un vecteur par position

Considérons trois tokens : « Le », « chat », « noir ». Chacun arrive avec un plongement initial et une information de position. Il serait tentant d'imaginer qu'ils sont aussitôt fondus en un unique vecteur représentant toute la phrase. Ce n'est pas ainsi que fonctionne le flux principal d'un transformeur génératif.

À chaque bloc, la séquence conserve un état par position. Trois tokens donnent donc trois colonnes de calcul. Les états montent en parallèle, même si leur contenu évolue. Des opérations intermédiaires peuvent élargir temporairement certaines dimensions, notamment dans les réseaux *feed-forward*, mais le flux résiduel revient à une largeur commune afin que les blocs puissent s'empiler.

Ce rappel prolonge la partie 1 sans la recommencer. Une entrée du vocabulaire donne un plongement initial ; une occurrence dans la séquence reçoit ensuite une représentation contextuelle. « Avocat » ne suit pas la même trajectoire auprès de « tribunal » que de « salade ». Ici, « noir » ne reste pas seulement l'étiquette d'une couleur : sa représentation est modifiée par ce qui précède.

La séquence n'est donc pas réduite à un résumé unique. Les informations peuvent être mélangées entre positions par l'attention, mais chaque colonne garde son emplacement dans la suite. C'est ce dispositif qui permet au modèle de calculer plusieurs états contextualisés à la fois pendant l'entraînement, tout en respectant l'ordre nécessaire à la génération.

## Transformer et échanger

Deux mouvements se combinent dans chaque bloc. Le premier travaille à une position donnée. Des couches linéaires et non linéaires transforment son état. Le second met les positions en relation : c'est l'**attention**.

Pour chaque position et chaque tête d'attention, le réseau construit schématiquement une requête, des clés et des valeurs. La requête de la position courante est comparée aux clés autorisées ; une softmax convertit ces compatibilités en poids ; la somme pondérée des valeurs fournit l'information échangée. Les calculs réels sont matriciels et parallèles. Dire qu'une position « consulte » les autres est une commodité pédagogique, pas la description d'un regard.

Dans un modèle génératif causal, une position peut utiliser sa propre position et celles qui la précèdent, jamais celles qui viennent après. Un masque causal bloque ces connexions futures. La première colonne de « Le chat noir » n'a accès qu'à « Le ». La deuxième peut combiner « Le » et « chat ». La troisième peut intégrer les trois positions. Elle est donc la seule à disposer de tout le préfixe lorsqu'il faut prédire la suite.

Après l'attention, le réseau *feed-forward* applique une transformation à chaque position séparément. Des connexions résiduelles conservent aussi un chemin continu à travers le bloc. L'attention échange ; le réseau local transforme ; les normalisations et les résidus stabilisent l'ensemble. Répété couche après couche, ce double mouvement fait évoluer les colonnes.

En bas, nous pouvons encore étiqueter la troisième colonne « noir », puisque son point de départ vient de ce token. En haut, l'étiquette devient trompeuse. L'état représente ce que le calcul a construit à cette position après intégration du préfixe « Le chat noir ». Les activations ainsi produites ne sont pas des connaissances nouvellement écrites dans le modèle. Elles existent pour cette séquence et ne modifient pas ses paramètres.

Toutes les positions ont été calculées, mais la génération lit l'état de la dernière. Ce choix n'exprime aucune noblesse particulière du dernier mot. Dans une architecture causale, cette position est simplement celle qui a pu intégrer tout le texte disponible.

## De l'état interne au vocabulaire

À la dernière couche, le modèle dispose donc d'un **état interne** pour la dernière position : un vecteur de nombres sans étiquettes lisibles. Pour produire une suite, il faut changer de question. Il ne s'agit plus de décrire l'état du calcul, mais d'évaluer la compatibilité de chaque token du vocabulaire avec cet état.

Une projection de sortie produit alors un score par token possible. Certains modèles réutilisent, transposée, la matrice de plongement employée à l'entrée ; d'autres possèdent des poids de sortie distincts. Cette réutilisation, appelée partage de poids, est fréquente mais non universelle.

Imaginons, après « Le chat », quatre scores fictifs :

| Token possible | Score |
|---|---:|
| dort | 8,2 |
| mange | 6,1 |
| noir | 4,9 |
| girafe | -1,3 |

Ces scores sont des **logits**. Ils peuvent être négatifs et ne totalisent pas 1. Ce ne sont pas encore des probabilités. Une fonction appelée **softmax** transforme l'ensemble des logits en valeurs positives dont la somme vaut 100 % :

| Token possible | Probabilité illustrative |
|---|---:|
| dort | 42 % |
| mange | 18 % |
| noir | 7 % |
| tous les autres | 33 % |

Les nombres de ces deux tableaux sont inventés pour rendre les étapes visibles ; ils ne proviennent d'aucun modèle mesuré. Le passage des logits aux probabilités ne rend pas l'état « plus sémantique ». Il associe simplement une probabilité calculée à chacune des étiquettes disponibles dans le vocabulaire.

Nous pouvons maintenant séparer quatre objets : l'état interne de la dernière position, les logits sur le vocabulaire, les probabilités après softmax et, enfin, le token effectivement retenu. Les confondre donne l'impression que le premier mot venu était déjà contenu dans le vecteur final. Il n'y était pas comme un objet caché : il résulte d'une comparaison, d'une normalisation et d'une procédure de sélection.

## Choisir n'est pas toujours prendre le premier

Prendre systématiquement le token le plus probable produit une génération dite gloutonne. De nombreux usages emploient plutôt un **échantillonnage** : le prochain token est tiré selon une distribution réglée. La température modifie les écarts entre logits avant la softmax. Une température basse concentre davantage la distribution ; une température plus élevée accorde relativement plus de poids aux candidats moins favorisés.

D'autres filtres peuvent limiter l'ensemble des candidats, par exemple aux tokens les mieux classés ou au plus petit groupe dont la probabilité cumulée dépasse un seuil. Les détails dépendent du système déployé. Ces réglages ne changent ni le corpus ni les paramètres appris ; ils agissent au moment de la génération.

La sélection n'est donc pas une décision au sens humain. C'est une procédure, parfois déterministe, parfois partiellement aléatoire, appliquée à la distribution produite par le modèle. Le token le plus probable peut perdre un tirage, et un token très peu probable peut être écarté par un filtre. Ce caractère réglable explique pourquoi une même demande peut recevoir des formulations différentes sans que le système ait changé d'avis entre les deux.

## La boucle

Le token retenu est ajouté au texte sous la forme de son identifiant. Il devient une nouvelle occurrence de la séquence. Le modèle doit maintenant prédire le token suivant en tenant compte de ce préfixe allongé. Projection, probabilités, sélection : la boucle se répète jusqu'à une marque d'arrêt ou une limite fixée par le système.

Une réponse n'est donc pas produite d'un bloc. Elle se construit token après token. À chaque étape, le contexte disponible comprend la demande de l'utilisateur, les instructions qui l'encadrent, les documents éventuellement fournis et les tokens déjà générés. Chaque nouvelle unité dépend de la séquence qui la précède. La machine ne déroule pas un texte qu'elle aurait auparavant rédigé en silence ; elle prolonge un préfixe, puis prolonge ce nouveau préfixe.

Cette description est une boucle conceptuelle. En production, un **cache de clés et de valeurs**, ou cache KV, évite généralement de recalculer à chaque tour toutes les opérations relatives aux tokens précédents. Le système conserve les résultats utiles de l'attention et calcule surtout la nouvelle position. L'optimisation change le coût du parcours, pas son principe autoregressif : un token est toujours produit à partir du contexte antérieur, puis réinjecté pour produire le suivant.

La cohérence d'un paragraphe peut ainsi émerger sans plan intégral fixé avant le premier mot. Elle dépend des régularités apprises, du contexte présent et des choix successifs. Cela n'interdit pas au modèle de produire des structures qui ressemblent à un plan ; cela interdit seulement d'en conclure qu'un texte complet attendait déjà derrière l'écran.

## Le plan de câblage n'explique pas la voix

Une résistance demeure : si nous avons décrit la chaîne, n'avons-nous pas décrit tout le comportement ? Non. Ce serait confondre un plan de câblage et ce qui circule dans le dispositif. Deux modèles d'architecture voisine peuvent répondre très différemment.

Le **corpus** fournit les régularités, les informations et les manières d'écrire rencontrées pendant le préentraînement. L'**entraînement** ajuste les paramètres pour la prédiction, puis le post-entraînement favorise certains comportements d'assistant. Le **contexte d'usage** conditionne enfin ce qui est mobilisé dans une conversation donnée. Aucun de ces trois niveaux ne se réduit au schéma des couches.

Le mécanisme permet donc d'expliquer comment une suite apparaît. Il n'explique pas, à lui seul, pourquoi elle adopte « nous », refuse une demande, rassure ou se montre péremptoire. Ces propriétés demandent d'examiner les voix apprises et la manière dont le post-entraînement en stabilise certaines.

> **Encadré récapitulatif — La chaîne en six opérations**
>
> | # | Opération | Ce qu'elle fait | Où cela se décide |
> |---|---|---|---|
> | 1 | Tokenisation | Découpe le texte et associe des identifiants | Tokenizer fixé pour le modèle |
> | 2 | Plongement | Fournit un vecteur initial par identifiant | Paramètres appris |
> | 3 | Position | Rend l'ordre utilisable dans le calcul | Architecture et paramètres |
> | 4 | Blocs de transformeur | Contextualisent les états par attention et transformations locales | Architecture et paramètres appris |
> | 5 | Projection de sortie | Produit des logits puis des probabilités sur le vocabulaire | Paramètres appris |
> | 6 | Sélection | Retient un token dans la distribution réglée | Procédure d'inférence |

Nous savons désormais comment une suite apparaît : les représentations se transforment, la dernière position est confrontée au vocabulaire, puis un token est choisi. Mais ce trajet n'explique pas pourquoi la continuation dit parfois « nos ancêtres », ni pourquoi elle se montre prudente ou péremptoire. Le calcul explique comment la suite apparaît ; il reste à comprendre qui semble parler.

## Références

- Ashish Vaswani et al., [« Attention Is All You Need »](https://arxiv.org/abs/1706.03762), 2017.
- Ofir Press et Lior Wolf, [« Using the Output Embedding to Improve Language Models »](https://arxiv.org/abs/1608.05859), 2016.
