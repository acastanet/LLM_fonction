La version tient, sauf sur un point où l'ajout casse quelque chose.

## La phrase à reprendre

> À la sortie, le modèle calcule une distribution de probabilités sur l'ensemble de son vocabulaire. Avec le dernier token et la matrice de plongement, puis une procédure de sélection détermine le prochain token.

La seconde phrase n'a pas de verbe principal cohérent, le « puis » reste orphelin. Je vois ce que vous voulez ajouter, et c'est une bonne idée : dire que la distribution ne sort pas de nulle part, qu'elle vient de la représentation du dernier token confrontée au vocabulaire. Deux façons de le poser.

Sobre :

> À la sortie, la représentation du dernier token est confrontée à l'ensemble du vocabulaire, ce qui donne une distribution de probabilités. Une procédure de sélection détermine alors le prochain token.

Avec le retour explicite à la matrice, puisque c'est ce que vous cherchiez :

> À la sortie, la représentation du dernier token est confrontée à l'ensemble du vocabulaire, souvent au moyen de la matrice de plongement lue cette fois dans l'autre sens. Le modèle obtient une distribution de probabilités, et une procédure de sélection détermine le prochain token.

Le « souvent » n'est pas de la prudence décorative : cette réutilisation de la même matrice en entrée et en sortie est fréquente mais pas universelle selon les modèles.

## Deux détails

Le retrait du passage sur le cache ne coûte rien à la démonstration. Il laisse seulement croire, à qui connaît le sujet, que tout est recalculé à chaque token. Vous pouvez l'assumer, la fiche ne parle pas d'implémentation.

Virgule d'articulation dans « une première phase ajuste les paramètres pour prédire la suite des textes, des phases complémentaires orientent ensuite ». Il manque un « puis » ou un point.

## Le découpage

Les retours à la ligne au milieu des phrases se transformeront en paragraphes une fois le texte rendu. Le triptyque corpus, apprentissage, contexte gagne d'ailleurs à être en trois paragraphes courts, c'est un rythme qui sert le propos. Mais la coupure à l'intérieur de la phrase sur l'apprentissage, elle, est involontaire.

Le reste est bon. La fin, en particulier, dit maintenant quelque chose de défendable au lieu de s'excuser.


# Un modèle ne répond pas, il continue

Vous écrivez une phrase, vous validez, un texte se déroule. L'impression est immédiate et presque irrésistible : quelqu'un a lu, quelqu'un a compris, quelqu'un a répondu. Très bien. Mais regardons précisément ce qui se passe entre votre question et le texte qui apparaît, car cet intervalle ne contient rien de ce que nous imaginons y mettre.

Il contient une chaîne d'opérations. Le tokenizer découpe d'abord le texte en tokens et attribue à chacun un identifiant, comme on attribuerait un numéro de rayon à un mot. La matrice de plongement transforme ces identifiants en vecteurs, et une information de position est introduite dans le calcul pour que l'ordre des tokens compte, car « le chien mord l'homme » et « l'homme mord le chien » ne mobilisent pas les mêmes numéros de rayon dans le même ordre. Ces vecteurs traversent ensuite une pile de blocs de transformeur. À la sortie, la représentation du dernier token est confrontée à l'ensemble du vocabulaire, ce qui donne une distribution de probabilités. Une procédure de sélection détermine alors le prochain token. Celui-ci est ajouté au texte, et tout recommence.

Voilà le premier point à tenir. Une réponse n'est pas produite d'un bloc, elle est produite token après token. À chaque étape, le modèle tient compte de tout le contexte disponible : votre demande, les consignes qui l'encadrent, les tokens qu'il vient lui-même d'écrire. Chaque nouveau token dépend de la séquence entière qui le précède. La machine ne rédige pas une réponse qu'elle aurait d'abord conçue. Elle prolonge un texte, une unité après l'autre, et c'est ce prolongement que nous appelons une réponse.

Il faut ici distinguer deux choses que le mot « représentation » recouvre sans les séparer. Entre l'entrée et la sortie, il ne circule plus des mots mais des tableaux de nombres. Chaque token dispose dans la matrice de plongement d'une ligne de quelques milliers de valeurs, sa représentation initiale, fixée une fois pour toutes à l'entraînement et identique quelle que soit la phrase. Puis, au fil des blocs, cette ligne est modifiée par le contexte. Le vecteur associé au mot « avocat » n'évolue pas de la même façon selon que le texte parle d'un tribunal ou d'une salade. La première représentation dort dans les paramètres, elle attend, elle est la même pour tout le monde. La seconde n'existe que pendant le calcul, pour cette séquence-là, et disparaît avec elle.

On pourrait objecter que décrire cette chaîne, c'est décrire la machine, et qu'il n'y a rien de plus à dire. Ce serait confondre le plan de câblage et le comportement. Deux modèles d'architecture comparable, entraînés autrement, produisent des résultats très différents. Le schéma ne dit pas pourquoi l'un se montre prudent et l'autre péremptoire, pourquoi l'un connaît la jurisprudence administrative française et l'autre non. Ce que nous appelons le comportement d'un modèle vient d'ailleurs, et de trois endroits.

Il vient d'abord du corpus d'entraînement, qui fournit les régularités de langue, les connaissances et les manières d'écrire que le modèle a rencontrées. Il vient ensuite de l'apprentissage lui-même. Une première phase ajuste les paramètres pour prédire la suite des textes, puis des phases complémentaires orientent le système vers les comportements attendus d'un assistant. Il vient enfin du contexte fourni au moment de l'usage : consigne système, demande de l'utilisateur, documents joints, conversation déjà écrite.

Deux opérations, remarquons-le, se tiennent en dehors du modèle proprement dit. Le tokenizer est arrêté avant l'entraînement, à partir d'un corpus, et il fixe pour toujours le vocabulaire et la manière de découper les textes. À l'autre extrémité, la sélection du prochain token relève d'une procédure appliquée au moment de l'usage. Des réglages comme la température y rendent le choix plus prévisible ou laissent davantage de place aux tokens moins probables. Le modèle est donc encadré, en amont et en aval, par des décisions qui ne sont pas les siennes.

Que reste-t-il alors dans nos mains ? Le corpus et l'entraînement sont achevés avant que nous ouvrions la fenêtre de discussion. Nous n'agissons sur eux qu'en choisissant un modèle plutôt qu'un autre, ce qui n'est pas rien mais ne se fait pas au fil de la journée. Notre prise directe se situe dans le contexte que nous construisons et, dans une moindre mesure, dans les réglages de sélection. Elle est réelle, et souvent décisive : une consigne précise, un document joint, un exemple bien choisi déplacent considérablement ce qui sort. Elle ne modifie pourtant ni les connaissances du modèle ni les dispositions qu'il a acquises. Elle détermine seulement ce qui en est mobilisé ici et maintenant.

C'est une marge de manœuvre étroite et sérieuse à la fois. Étroite, parce que nous ne rendrons pas savant un modèle qui ignore notre discipline, et qu'aucune formulation habile ne remplacera un entraînement. Sérieuse, parce que tout ce qui, dans une réponse, nous paraît relever du jugement de la machine relève en réalité d'un contexte que quelqu'un a écrit. Lundi matin, devant une classe, cette phrase a une conséquence directe : la qualité de ce qui sort de l'outil est en grande partie la trace de ce que nous y avons mis. Il ne s'agit donc pas de savoir si la machine comprend. Il s'agit de savoir ce que nous avons placé dans son contexte, et si nous sommes capables d'en répondre.

---

**Réserve, puisque vous la demandez.** Le style CVGZ vous coûte quelque chose ici. Le texte gagne en tenue et en portée, mais il perd sa fonction de fiche : les six éléments de la chaîne, qui étaient auparavant repérables d'un coup d'œil, sont maintenant fondus dans un paragraphe continu. Un lecteur qui cherche à vérifier l'ordre des opérations devra relire. Le guide lui-même le signale au paragraphe 16.2, un texte pédagogique demande des phrases plus courtes, un seul paradoxe principal, une conclusion sous forme de critère. J'ai poussé le curseur vers l'essai. Si cette page doit rester une fiche dans la série, la version précédente sert mieux, et celle-ci ferait un bon texte d'ouverture ou de clôture pour l'ensemble.

## Fiche — Comment une réponse est produite

Le texte d'ouverture de cette fiche pose la question autrement. Ici, on garde l'ordre des opérations et les repères vérifiables.

### La chaîne, en six opérations

| # | Opération | Ce qu'elle fait | Où cela se décide |
|---|---|---|---|
| 1 | Tokenisation | Découpe le texte en tokens et attribue à chacun un identifiant | Vocabulaire arrêté avant l'entraînement, à partir d'un corpus |
| 2 | Plongement | Transforme chaque identifiant en un vecteur de quelques milliers de valeurs | Valeurs fixées par l'entraînement |
| 3 | Position | Introduit dans le calcul l'ordre des tokens dans la séquence | Mécanisme fixé par l'architecture |
| 4 | Pile de blocs de transformeur | Modifie chaque vecteur en fonction du contexte de la séquence | Paramètres fixés par l'entraînement |
| 5 | Projection de sortie | Confronte la représentation du dernier token à l'ensemble du vocabulaire, ce qui donne une distribution de probabilités | Paramètres fixés par l'entraînement |
| 6 | Sélection | Choisit un token dans cette distribution | Réglée au moment de l'usage (température et échantillonnage) |

### La boucle

Le token choisi est ajouté au texte, et la chaîne reprend à l'opération 1 pour produire le suivant.

Une réponse n'est donc pas produite d'un bloc. Elle est produite token après token. À chaque étape, le modèle tient compte de tout le contexte disponible : la demande de l'utilisateur, les consignes qui l'encadrent et les tokens qu'il vient lui-même d'écrire.

### Deux représentations à ne pas confondre

**La représentation initiale.** Une ligne de la matrice de plongement. Fixée une fois pour toutes à l'entraînement, identique quelle que soit la phrase, stockée dans les paramètres du modèle.

**Les représentations contextuelles.** Le même vecteur, modifié au fil des blocs par ce qui l'entoure. Le mot « avocat » n'évolue pas de la même façon selon que le texte parle d'un tribunal ou d'une salade. Ces représentations n'existent que pendant le calcul, puis disparaissent avec la séquence.

### Deux opérations hors du modèle

La tokenisation et la sélection encadrent le modèle proprement dit. L'une est arrêtée avant l'entraînement, l'autre s'applique au moment de l'usage. Aucune des deux n'est apprise par le réseau lui-même.

### D'où vient le comportement

Décrire la chaîne revient à dessiner un plan de câblage. Cela n'explique pas le comportement, car deux modèles d'architecture comparable, entraînés autrement, produisent des résultats très différents.

| Source | Ce qu'elle apporte | Quand elle est fixée | Notre prise |
|---|---|---|---|
| Corpus d'entraînement | Régularités de langue, connaissances, manières d'écrire | Avant l'usage | Choix du modèle |
| Entraînement | Une première phase pour prédire la suite des textes, puis des phases complémentaires orientant vers les comportements d'un assistant | Avant l'usage | Choix du modèle |
| Contexte | Consigne système, demande, documents joints, conversation déjà écrite | Au moment de l'usage | Directe |

### Critère de travail

Notre marge est réelle mais située. Elle ne modifie ni les connaissances du modèle ni les dispositions qu'il a acquises. Elle détermine ce qui en est mobilisé ici et maintenant.

En pratique, devant un résultat décevant, la question utile n'est pas « le modèle a-t-il compris ». Elle est en deux temps :

1. Ce que j'attends se trouve-t-il dans ce que ce modèle a appris ? Si non, aucune formulation ne le fera apparaître, il faut changer de modèle ou fournir la source.
2. Si oui, mon contexte l'a-t-il rendu mobilisable ? C'est là que se joue la reprise.

### À retenir

- Un modèle ne rédige pas une réponse conçue à l'avance, il prolonge un texte token après token.
- Entre l'entrée et la sortie, il ne circule plus des mots mais des tableaux de nombres.
- La représentation d'un token en entrée est la même pour tous les contextes, celle qui traverse les blocs ne l'est pas.
- Le comportement vient du corpus, de l'entraînement et du contexte, dans cet ordre d'antériorité.
- Notre seule prise directe est le contexte, et accessoirement les réglages de sélection.

---

Deux remarques sur l'usage de cette fiche.

Le tableau des six opérations recoupe la fiche 03 sur les points 1 et 2. Si les deux se suivent dans le tiré à part, une ligne de renvoi vaut mieux qu'une reprise : la fiche 03 explique la carte, celle-ci explique le trajet.

Pour l'infographie 4:3, l'idée à porter est la boucle, pas la liste. Six cases alignées se lisent comme un tuyau à sens unique, ce qui est précisément le contresens à éviter. Une flèche de retour depuis le token produit vers l'entrée, et les cases 1 et 6 posées hors du cadre du modèle, suffiraient à dire l'essentiel de la fiche.