# Une phrase dans la machine

## Guide d’articulation et de finalisation de la série

**Version :** 1.2 — 27 septembre 2026<br>
**Point de départ :** les cinq textes déjà rédigés et les intentions précisées dans la conversation.  
**État du travail :** environ 75 % de la rédaction est réalisée, selon l’estimation de l’auteur.  
**Travail restant :** trouver la bonne articulation, préciser les intentions de lecture et effectuer des ajustements à la marge.

**Mise à jour 1.2 :** ajout d’un repère éditorial sur le *reward hacking* pour la partie 4, avec une note orale correspondante dans le support de présentation.

Ce guide corrige la version 1.0, qui proposait une transformation trop importante des manuscrits. Les textes existants constituent la base de publication. Leurs titres, leurs exemples, leur voix et l’essentiel de leur développement sont conservés. La nouvelle orientation précise leur lecture commune : présenter des recherches qui permettent de regarder les LLM autrement.

Les décisions éditoriales antérieures continuent de guider les points compatibles avec cette articulation. Le présent document précise l’insertion du texte sur le grokking, les raccords entre articles et quelques inflexions de présentation. Les cinq articles ne sont pas à réécrire selon un nouveau gabarit.

### Référence stylistique obligatoire

Le [guide `styleCVGZ.md`](styleCVGZ.md) est essentiel et doit être appliqué à toute rédaction ou retouche : ouvertures, transitions, développements et conclusions. Le lire avant d’intervenir et relire les modifications à sa lumière. Ses consignes de voix, de rythme, de structure et de vocabulaire font partie des critères de finalisation.

Conserver notamment son mouvement : partir d’une question concrète, installer une difficulté, distinguer les notions, traverser un exemple ou une recherche, accueillir une objection et revenir aux conséquences humaines. Les raccords doivent prolonger la voix des textes existants. Les plans du présent document servent leur articulation ; ils ne remplacent pas les exigences stylistiques de `styleCVGZ.md`.

## 1. L’intention commune issue de la conversation

La série propose une vulgarisation scientifique nourrie de recherches, de résultats surprenants et d’hypothèses. Elle permet de découvrir pourquoi certaines descriptions habituelles des LLM demandent à être enrichies.

Trois intentions exprimées par l’auteur lui donnent sa cohérence :

- **« Numériser » les mots ne suffit pas à conclure que le langage est dénaturé.** Montrer ce que les représentations numériques permettent de conserver, de mettre en relation et de transformer. La précision du mécanisme sert cette interrogation.
- **Généraliser est possible pour une machine.** L’expérience du grokking permet d’examiner ce qui dépasse la restitution des exemples rencontrés. Elle donne matière à discuter l’image d’une simple base de données, dans les limites de la tâche étudiée.
- **Parler de personnalité est possible même à propos de machines.** Présenter l’hypothèse comme un outil pour comprendre des régularités de comportement et envisager des prédictions. Préciser le sens du terme et la portée des observations.

Le lecteur est invité à rencontrer ces questions à travers les travaux déjà présents dans les manuscrits. Les explications techniques permettent de suivre les recherches. La série ne vise pas à couvrir systématiquement toutes les composantes d’un LLM.

**Promesse de lecture proposée :**

> Des mots deviennent des représentations numériques. Un réseau peut réussir au-delà des exemples qu’il a rencontrés. Une hypothèse de personnalité peut éclairer le comportement d’un assistant. Que nous apprennent ces recherches sur les LLM et sur la manière de les utiliser ?

L’ensemble doit permettre une ouverture intellectuelle réelle. La prudence scientifique précise ce que l’on peut conclure ; elle ne doit pas neutraliser chaque découverte par un rappel répétitif des limites des machines.

## 2. L’articulation recommandée

**Ordre de lecture : les actuels articles 1 → 2 → le texte sur le grokking → l’actuel article 3 → l’actuel article 4.**

| Rang dans la série | Texte existant, titre conservé | Rôle dans le parcours |
| --- | --- | --- |
| 1 | **Comment le texte arrive au modèle ?** | Comprendre ce que la représentation numérique rend possible. |
| 2 | **Un modèle ne répond pas, il continue** | Suivre la production d’une réponse et poser la question des capacités mobilisées. |
| 3 | **Grokking : quand un réseau généralise après avoir déjà mémorisé** | Examiner, par une recherche précise, la différence entre réussir des exemples et généraliser. |
| 4 | **Qui parle quand une machine répond ?** | Explorer l’hypothèse des personnages et des régularités de comportement. |
| 5 | **Aligné avec quoi — et surtout avec qui ?** | Interroger les finalités et les responsabilités qui orientent le système. |

Les numéros des dossiers et les noms des fichiers restent des repères documentaires. Le texte situé dans `5_Grokking/` devient le troisième dans l’ordre de lecture proposé.

### Pourquoi cet ordre tient

Les deux premiers articles forment déjà un ensemble : l’entrée du texte, puis la production de sa continuation. Leur enchaînement reste intact.

Le grokking intervient ensuite comme une enquête sur l’apprentissage. Le lecteur vient de suivre ce que fait un modèle lorsqu’il répond ; il examine maintenant comment une capacité peut se former pendant l’entraînement. Ce changement de moment doit être annoncé en une phrase pour éviter de laisser croire que le réseau se réentraîne pendant chaque conversation.

L’article sur les personnages prolonge la question des capacités acquises vers celle des comportements. La généralisation du grokking et l’hypothèse des personas portent sur des objets différents : leur succession constitue une progression de lecture, pas une démonstration que la première prouverait la seconde.

L’alignement conserve sa place de conclusion. Le passage du personnage au comportement souhaité, puis aux personnes qui en déterminent les finalités, est déjà construit dans les deux derniers manuscrits.

## 3. Plan détaillé à partir des textes existants

### 3.1. Comment le texte arrive au modèle ?

**Fichier de référence :** [article 1](<1 _Matrice/article_01_comment_le_texte_arrive.md>).

**Intention de lecture.** Faire comprendre que transformer le texte en représentations numériques permet de travailler sur des relations linguistiques. La question du langage donne son intérêt au trajet technique.

**Base à conserver.** La phrase du sucre, les distinctions mot/token et identifiant/vecteur, les exemples d’« anticonstitutionnellement » et d’« avocat », la distinction entre plongement initial et représentation contextuelle.

| Section existante | Fonction dans la lecture | Ajustement ciblé |
| --- | --- | --- |
| La phrase à l’écran | Partir de l’expérience familière d’écrire. | Faire apparaître plus tôt l’enjeu : ce que le passage aux nombres permet de représenter. |
| Le modèle ne reçoit pas des mots | Introduire les unités traitées. | Conserver l’explication et l’exemple ; alléger une formulation si elle freine la lecture. |
| Un numéro qui ne signifie rien | Distinguer l’index de la représentation. | Garder cette distinction courte et concrète. |
| Le casier contient un vecteur | Faire comprendre l’utilité du vecteur. | Mettre en valeur la possibilité de calculer des relations. |
| Une carte apprise, pas un dictionnaire | Introduire la structure acquise et ses limites. | Relier explicitement ce passage aux travaux déjà cités. |
| Le premier vecteur n’est qu’un départ | Montrer l’effet du contexte. | Conserver « avocat » et la distinction actuelle, sans ajouter de nouvelles couches d’explication. |
| Ce qu’il faut retenir | Rassembler les distinctions. | Ajouter une phrase de portée générale avant le raccord vers la génération. |

**Place des recherches.** Les références existantes sur la tokenisation et les transformeurs fournissent les appuis. Une courte phrase dans le corps du texte peut préciser la question à laquelle ces travaux répondent. Une nouvelle expérience ne devient pas le centre obligatoire de l’article.

**Point d’attention.** L’ouverture peut être rendue plus invitante sans déplacer toutes les sections. La métaphore du vestiaire reste possible dans le texte ; les restrictions propres aux infographies continuent de s’appliquer à ces supports.

### 3.2. Un modèle ne répond pas, il continue

**Fichier de référence :** [article 2](2_Traitement/article_02_un_modele_continue.md).

**Intention de lecture.** Montrer comment une continuation se construit, en laissant ouverte la question de ce que le modèle a appris pour la produire. La génération progressive ne suffit pas à réduire la richesse des capacités mobilisées.

**Base à conserver.** Le texte qui se déroule à l’écran, l’exemple « Le chat noir », les états par position, la boucle et la distinction corpus/entraînement/contexte.

| Section existante | Fonction dans la lecture | Ajustement ciblé |
| --- | --- | --- |
| Vous écrivez une phrase, le texte se déroule | Installer le décalage entre impression et production. | Conserver la scène ; faire sentir l’intérêt de comprendre cette génération. |
| Un vecteur par position | Prolonger l’article 1. | Maintenir le rappel utile et supprimer seulement les répétitions manifestes. |
| Transformer et échanger | Expliquer le rôle des transformations et de l’attention. | Alléger localement le passage le plus dense si nécessaire, sans reconstruire l’article. |
| De l’état interne au vocabulaire | Relier le calcul à une suite possible. | Garder la progression et les exemples. |
| Choisir n’est pas toujours prendre le premier | Expliquer la sélection et la variation. | Conserver les réglages déjà présentés. |
| La boucle | Donner une vue d’ensemble. | Rendre bien visible le contexte déjà mentionné : instructions, demande, documents et texte produit. |
| Le plan de câblage n’explique pas la voix | Distinguer mécanisme et origine des comportements. | Maintenir l’annonce de la voix, mais intercaler la question de la généralisation dans la conclusion. |

**Place des recherches.** Les travaux déjà cités expliquent la construction étudiée. Le texte sert de passage entre les représentations et les capacités acquises ; il n’a pas à devenir une enquête entièrement nouvelle sur Othello.

**Point d’attention.** Le titre est conservé. Le corps du texte doit permettre au lecteur de comprendre que « continuer » décrit un mode de production dont il reste à examiner les possibilités. Le paragraphe sur l’entraînement sert de repère ; le grokking lui donne ensuite une incarnation expérimentale.

### 3.3. Grokking : quand un réseau généralise après avoir déjà mémorisé

**Fichier de référence :** [texte sur le grokking](5_Grokking/grokking_generalisation_modifie.md).

**Intention de lecture.** Faire découvrir, à travers l’histoire d’une recherche, une capacité qui ne se laisse pas décrire comme la seule restitution d’exemples appris.

**Base à conserver.** L’ouverture sur les bonnes réponses, l’horloge, la séparation entre données d’entraînement et exemples réservés, le récit de l’expérience prolongée et le décalage des performances.

Le texte possède déjà sa progression. Ses relances en gras peuvent continuer à tenir lieu d’étapes ; il n’est pas nécessaire de lui imposer les sept sections des autres articles.

1. **Une réussite qui pose question.** Garder le contraste initial entre réussite sur les exemples rencontrés et réussite sur de nouveaux exemples.
2. **Le problème expérimental.** Conserver l’opération modulaire et l’explication du partage des données.
3. **Une situation qui semblait stabilisée.** Faire suivre les performances sur l’entraînement et l’évaluation comme le fait déjà le texte.
4. **L’expérience qui continue.** Préserver le récit en gardant son attribution. Les détails anecdotiques et les chiffres devront correspondre aux sources citées.
5. **La généralisation devient observable.** Garder le retournement central et l’apparition du terme grokking après le phénomène.
6. **Ce que cette recherche change.** Conserver la portée délimitée de l’expérience ; ajouter seulement le raccord vers les comportements abordés ensuite.

**Place des recherches.** Power et ses collègues ainsi que le témoignage cité structurent déjà cet article. La préparation finale porte sur la fidélité aux sources existantes ; elle ne suppose pas d’ajouter un historique complet des recherches sur le grokking.

**Point d’attention.** Son format plus court peut être conservé : il forme une respiration expérimentale entre deux ensembles plus denses. La cible de longueur des quatre articles initiaux ne justifie pas de l’allonger artificiellement. Distinguer dans le raccord entraînement du modèle et utilisation en conversation.

### 3.4. Qui parle quand une machine répond ?

**Fichier de référence :** [article sur la voix](<3_Qui parle/article_03_qui_parle_version_serie.md>).

**Intention de lecture.** Montrer pourquoi l’hypothèse de personnalité ou de personnage mérite d’être examinée scientifiquement, y compris lorsqu’il s’agit de machines.

**Base à conserver.** « Nos ancêtres », le récit Linda–David, la présentation du PSM, les expériences qui l’éclairent, ses contre-épreuves et l’ouverture sur l’alignement.

| Section existante | Fonction dans la lecture | Ajustement ciblé |
| --- | --- | --- |
| Une phrase de trop : « nos ancêtres » | Faire apparaître l’énigme. | Conserver cette ouverture forte. |
| Ce que prédire exige | Relier prédiction et régularités de personnages. | Ajouter, si utile, une phrase de rappel de la généralisation, avec sa différence d’objet. |
| L’hypothèse du personnage | Présenter le raisonnement des chercheurs. | Définir le lien entre personnalité, persona et rôle sans changer l’architecture. |
| Les expériences qui soutiennent cette lecture | Montrer les appuis de l’hypothèse. | Conserver les expériences à leur place, notamment le désalignement émergent. |
| Ce que cette hypothèse change techniquement | Donner une conséquence au modèle explicatif. | Maintenir l’exemple de refus ; un bref rapprochement avec AnSu est possible. |
| Ce qu’elle ne tranche pas | Éprouver la portée de l’explication. | Conserver les limites et le contre-exemple, sans répéter les réserves dans chaque paragraphe. |
| Aligner quel personnage ? | Ouvrir la question des finalités. | Garder le raccord déjà construit. |

**Place des recherches.** Le PSM est déjà l’axe du manuscrit. Il n’est pas nécessaire de le remplacer par une nouvelle étude. La relecture doit surtout rendre sensible l’utilité de cette hypothèse pour comprendre et anticiper des comportements.

**Point d’attention.** « Personnalité » peut désigner ici un ensemble de dispositions comportementales étudiées. Préciser ce sens permet de poser la question sans assimiler toutes les propriétés d’un assistant à celles d’une personne. Éviter de présenter l’hypothèse comme automatiquement disqualifiée par son vocabulaire humain.

### 3.5. Aligné avec quoi — et surtout avec qui ?

**Fichier de référence :** [article sur l’alignement](4_Alignement/article_04_aligne_avec_qui.md).

**Intention de lecture.** Conduire la série des comportements observés aux finalités et aux responsabilités qui leur donnent une orientation.

**Base à conserver.** La scène de l’élève, la distinction obéissance/alignement, l’alignement direct et social, le système complet et la décision humaine finale.

| Section existante | Fonction dans la lecture | Ajustement ciblé |
| --- | --- | --- |
| L’assistant obéit. Est-ce suffisant ? | Poser le problème à partir d’un usage familier. | Conserver l’ouverture. |
| Aligné avec quoi et avec qui ? | Faire apparaître la pluralité des finalités. | Garder les acteurs et les distinctions. |
| Une relation, pas une vertu de la machine | Préciser le sens de l’alignement. | Relire la définition pour sa fluidité. |
| Alignement direct et alignement social | Donner un outil pour penser les effets. | Mettre en valeur les recherches déjà mobilisées et illustrer l’écart entre objectif visé et récompense mesurée par le *reward hacking*. |
| Le système, pas seulement le modèle | Situer les consignes, l’interface, les outils et les responsabilités. | Utiliser éventuellement AnSu comme illustration courte. |
| Fixer, vérifier, maintenir | Relier l’intention aux observations. | Conserver la logique de supervision. |
| Ce que nous ne pouvons pas déléguer | Conclure le parcours. | Ajouter la généralisation dans le bilan de la série et actualiser les renvois. |

**Place des recherches.** Le rapport, les travaux sur les valeurs et les distinctions entre objectifs directs et sociaux sont déjà présents. La finalisation doit montrer leur apport au raisonnement. Les références institutionnelles accompagnent cette réflexion sans devenir un catalogue.

**Ajout ciblé — *reward hacking*.** Présenter brièvement le cas où l’optimisation d’une récompense imparfaite s’écarte de l’objectif qu’elle devait représenter. Le situer comme un problème de spécification et de vérification technique, sans le confondre avec l’ensemble de l’alignement social. « Tricher » ou *game-playing* peut servir d’image, à condition de ne pas prêter à l’agent une intention humaine. Pour le manuscrit, s’appuyer sur Skalse et al., [*Defining and Characterizing Reward Hacking*](https://arxiv.org/abs/2209.13085) ; les [exemples de Google DeepMind](https://deepmind.google/blog/specification-gaming-the-flip-side-of-ai-ingenuity/) peuvent nourrir la présentation. La note orale est déjà ajoutée à la [diapo 8 du plan de présentation](<Présentation/nouveau_plan_8_diapos_coherent.md>). Le [README du dossier](<4_Alignement/README.md>) précise le rôle des matériaux et la réserve sur les sources.

**Point d’attention.** Cet article reste l’aboutissement déjà rédigé. Il n’est pas reconstruit autour d’une expérience de désalignement déplacée depuis le précédent ; le *reward hacking* reste un exemple bref au service de la distinction entre la cible et sa mesure.

## 4. Les raccords : le principal travail rédactionnel restant

Les formulations suivantes sont des propositions de transition, à adapter au rythme des textes.

### De l’article 1 à l’article 2

Le raccord actuel fonctionne. Une inflexion positive suffit :

> Le texte est devenu calculable, et ses représentations peuvent être transformées en fonction du contexte. Reste à suivre ce que ces opérations rendent possible : la production d’une continuation.

### De l’article 2 au grokking

Ce raccord remplace la promesse d’un passage immédiat à la voix :

> Nous avons suivi la manière dont une réponse se construit. Mais comment apprécier ce que le modèle a appris pour la produire ? Avant de revenir à la voix de l’assistant, une expérience permet de regarder de plus près la différence entre réussir les exemples rencontrés et généraliser.

Au début du grokking, une phrase suffit pour marquer le changement de moment :

> Quittons un instant la conversation avec un modèle déjà entraîné pour observer ce qui peut se passer pendant son apprentissage.

### Du grokking à l’article sur les personnages

> Cette expérience porte sur une tâche mathématique précise. Les assistants conversationnels nous posent une autre question : comment leurs manières de répondre se retrouvent-elles dans des situations différentes ? Des chercheurs proposent de les examiner à travers une hypothèse de personnage.

Le chapeau de l’article sur la voix pourra rappeler en une phrase les deux acquis précédents : génération progressive et question de la généralisation. Son ouverture sur « nos ancêtres » reste en place.

### Des personnages à l’alignement

Conserver l’articulation existante : « le personnage que nous voulons » conduit déjà à demander qui est ce « nous » et quelles conduites il souhaite favoriser. Une réécriture serait utile seulement si une répétition apparaît après assemblage.

### Conclusion de la série

Retoucher le bilan final pour faire tenir les cinq déplacements : représenter les mots, produire une continuation, généraliser, examiner les personnalités, orienter les comportements. La responsabilité de l’enseignant et des autres acteurs reste la conclusion pratique.

## 5. AnSu : éclairer la lecture sans déplacer le centre de la série

Les informations ajoutées sur AnSu permettent des rapprochements précis. L’agent naïf est un de ses cas d’usage : l’élève explique, l’agent relance et restitue, l’enseignant interprète les échanges et organise la suite.

Privilégier les liens les plus féconds, dans les deux derniers articles :

- **Personnages :** comment un modèle capable de fournir une explication peut-il tenir le rôle d’un novice qui demande des précisions ?
- **Alignement :** pourquoi, dans cette activité, la réponse attendue de l’agent dépend-elle de la finalité pédagogique et de la supervision ?

Le grokking peut susciter une remarque sur ce que quelques essais réussis permettent d’affirmer. Le rapprochement doit rester explicitement une question d’évaluation, sans assimiler entraînement d’un réseau et essais d’un agent configuré.

L’encadré « Ce que cela change avec AnSu » n’est pas obligatoire dans chaque article. Une référence locale et bien située suffit. Les PDF du dossier servent à décrire le dispositif et ses intentions ; les bénéfices attendus y sont distingués des résultats encore à établir. Les documents v7 et v7.5 ne doivent pas être fusionnés en une description technique unique.

## 6. Une passe éditoriale limitée et cohérente

### Ce qui reste acquis

Conserver les titres, les exemples, les scènes, les études déjà mobilisées, les développements qui fonctionnent et la voix des manuscrits. La trame discutée — scène, difficulté, distinction, recherche, limite, conséquence — sert de grille de lecture souple. Elle n’impose pas de remodeler les cinq textes.

Les travaux scientifiques doivent être perceptibles dans le récit : un nom, une question de recherche ou une référence intégrée peut parfois suffire. Tous les articles n’ont pas besoin de commencer par une expérience nouvelle. Les deux premiers rendent les objets de recherche intelligibles ; le grokking et les personas donnent des enquêtes plus directement centrées sur une étude ; l’alignement prolonge leurs enjeux.

### Les interventions à effectuer

1. Relire les cinq textes dans l’ordre proposé pour repérer les seules ruptures de logique.
2. Retoucher les chapeaux et les conclusions afin de rendre l’intention commune visible.
3. Insérer les raccords autour du grokking et conserver ceux qui fonctionnent déjà.
4. Alléger localement les passages techniques les plus denses, sans remplacer les développements.
5. Corriger les répétitions réelles ; conserver les brefs rappels nécessaires à une lecture autonome.
6. Vérifier les affirmations et les sources mobilisées lors de la relecture finale, sans élargir systématiquement le corpus.
7. Harmoniser les numéros de partie, les renvois et les métadonnées une fois les cinq textes assemblés. Le texte sur le grokking recevra les champs de série utiles ; son statut de relecture devra correspondre aux vérifications réellement faites.
8. Vérifier ensuite les illustrations et leurs légendes ; les refaire seulement si elles contredisent le texte final.

### Limite de cette passe

Aucun nouvel article sur l’entraînement, Othello ou les circuits multilingues n’est nécessaire pour obtenir la cohérence recherchée. Ces pistes de la version précédente du guide sont retirées du plan de travail. L’enrichissement éventuel d’une référence ne doit pas devenir le prétexte à remplacer un manuscrit.

Le titre de collection **« Une phrase dans la machine »** reste utilisable. Le sous-titre et l’annonce peuvent mieux mettre en avant les recherches et le changement de regard. Les documents éditoriaux antérieurs sont à actualiser sur les points réellement concernés, notamment le passage de quatre à cinq articles.

## 7. Critères de réussite

- Les cinq textes existants restent reconnaissables dans leurs titres, exemples et développements.
- L’ordre fait apparaître une progression sans demander au lecteur un apprentissage technique exhaustif.
- Les trois intentions de la conversation sont lisibles : représenter le langage, généraliser, examiner l’hypothèse des personnalités.
- Les recherches donnent de la matière à penser et sont attribuées avec une portée claire.
- Le détour par l’apprentissage est distingué du déroulement d’une conversation.
- La généralisation sur une tâche et l’hypothèse de persona sont reliées par une question, sans être confondues.
- AnSu éclaire certains enjeux et conserve sa juste place de prolongement pédagogique.
- Les dernières retouches améliorent les transitions et la lecture plutôt qu’elles n’ouvrent de nouveaux chantiers.

**La question de relecture finale :** les cinq articles donnent-ils désormais le sentiment d’une même série, tout en conservant ce qui fait déjà la force de chacun ?
