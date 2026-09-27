# Une phrase dans la machine
## Plan du document autoportant, 10 pages plus une page de références

Ce plan décrit ce qui figure sur chaque page : titre, message clé, composition visuelle, notions définies, mentions obligatoires. Les paragraphes d'appui font l'objet d'un document séparé, « Commentaire des 10 pages ».

---

# 1. Règles communes

## Format

- Portrait, A4 ou 4:3. Schéma dans les deux tiers supérieurs, zone de texte en dessous.
- Un seul schéma dominant par page. La page 9 est la seule exception assumée, avec un encadré secondaire.
- Pagination visible et titre de la série en pied de page.

## Style

- Papier découpé semi réaliste, texture légère, ombres douces, lumière venant du haut à gauche.
- Fond blanc majoritaire, texte noir sur cartes blanches.
- Formes simples : cartes, cercles, flèches, matrices, bulles de dialogue.
- Aucun décor sans fonction informative. Ni corps, ni visage, ni cerveau, ni robot.

## Code couleur, pages 1 à 7

- Bleu : texte, contexte, entrée.
- Orange : transformation ou calcul.
- Vert : représentation produite ou comportement stabilisé.
- Jaune : élément mis en évidence, token retenu ou mot souligné.
- Rouge : un seul usage, la limite ou le contrôle. Jamais pour signaler une idée fausse ou une mauvaise réponse.

## Code couleur, pages 8 à 10

Le sens des couleurs change et ce changement est annoncé en clair sur la page 8. Les couleurs ne désignent plus des étapes de calcul mais des fonctions humaines.

- Bleu : normes et finalités.
- Orange : vérifications et mesures.
- Vert : maintien, rôles, responsabilités.
- Rouge : droits non négociables, limites, arrêt.

## Mentions obligatoires

- Sous tout schéma comportant des nombres : « valeurs illustratives, elles ne proviennent d'aucun modèle mesuré », en italique.
- Sous tout schéma comportant un découpage en tokens : « découpage pédagogique, il dépend du tokenizer ».
- En pied de page : renvoi à la partie source de la série, avec son titre complet.

## Notions définies

Format fixe : terme, deux points, définition de quinze mots maximum. Aucun terme n'apparaît nu.

## Continuité des exemples

- Question fil rouge des pages 1 à 7 : « Pourquoi aimons-nous le sucre ? »
- Token de référence des pages 2 et 3 : « sucre ».
- Continuation de référence des pages 4 à 6 : « Parce que nos ancêtres… »
- Changement d'exemple en page 7, annoncé sur la page comme comparaison comportementale.
- Scène de référence des pages 8 à 10 : l'exercice de géométrie du lundi matin.
- Mention en page 1 : les exemples chiffrés sont recomposés pour ce document et diffèrent de ceux des articles.

---

# 2. Plan des pages

## Page 1. Une phrase dans la machine

**Message clé.** Suivre une phrase depuis sa saisie jusqu'aux choix humains qui encadrent la réponse.

**Composition.** Une frise en quatre étapes, disposée sur deux rangées.

1. Entrée : carte bleue portant la question fil rouge.
2. Génération : suite de tokens et flèche orange.
3. Voix : bulle de dialogue verte.
4. Encadrement : carte blanche cerclée de noir portant quatre questions abrégées, un accent rouge sur « qui peut arrêter ».

Sous la frise, un bloc « contrat de lecture » en trois lignes : ce que le document traite, ce qu'il ne traite pas, le statut des chiffres montrés.

**Notions.**

- série : quatre parties, de l'entrée du texte aux conditions d'usage
- token : unité de travail obtenue par découpage du texte
- voix apparente : impression qu'un locuteur parle, examinée en page 6
- encadrement : décisions humaines qui fixent finalité et limites

**Renvoi.** Série complète, parties 1 à 4.

---

## Page 2. Ce que reçoit réellement le modèle

**Message clé.** Le modèle reçoit une suite ordonnée d'unités calculables, pas une phrase déjà comprise.

**Composition.** Une chaîne en cinq étapes, sur deux rangées, orientation constante de gauche à droite.

1. Phrase : carte bleue, « Pourquoi aimons-nous le sucre ? »
2. Tokens : cartes bleues séparées, découpage illustratif.
3. Identifiants : un nombre entier noir sous chaque token, sans couleur, pour marquer qu'il ne mesure rien.
4. Vecteurs initiaux : une colonne de valeurs par token, avec un indice de rang au sommet de chaque colonne, légendé « information de position ».
5. Représentations contextuelles : mêmes positions, colonnes vertes, transformées par le contexte.

**Notions.**

- caractères encodés : nombres associés aux signes du texte, avant tout découpage
- token : unité de travail, mot entier, fragment ou signe de ponctuation
- identifiant : numéro qui désigne une entrée du vocabulaire, sans la décrire
- vecteur de plongement : ligne de valeurs numériques associée à un identifiant
- information de position : donnée qui rend l'ordre des tokens utilisable dans le calcul

**Mentions.** Découpage pédagogique dépendant du tokenizer. Valeurs illustratives.

**Renvoi.** Partie 1, « Comment le texte arrive au modèle ? »

---

## Page 3. Désigner et représenter

**Message clé.** L'identifiant désigne une ligne, le vecteur est cette ligne. Ce sont deux opérations distinctes.

**Composition.** Un enchaînement vertical de cinq éléments, centré sur le token « sucre ».

1. Token : carte bleue, « sucre ».
2. Identifiant : le nombre 902, en noir, isolé.
3. Matrice de plongement : un tableau de lignes, une seule ligne surlignée en vert.
4. Vecteur initial : la même ligne extraite et posée à côté du tableau, strictement du même vert, avec quatre valeurs visibles suivies de points de suspension.
5. Représentation contextualisée : le vecteur replacé dans la phrase complète, vert plus soutenu.

Entre les éléments 2 et 4, deux verbes en gros caractères, **désigner** et **représenter**, chacun relié à l'élément qu'il commande.

**Notions.**

- désigner : indiquer quelle entrée du vocabulaire est concernée
- représenter : fournir des valeurs sur lesquelles le calcul peut porter
- matrice de plongement : tableau contenant une ligne par entrée du vocabulaire
- vecteur appris : ligne ajustée pendant l'entraînement, point de départ de la prédiction

**Interdit.** Aucune métaphore de vestiaire, de ticket ou de casier. Aucun objet extérieur au dispositif.

**Mentions.** L'identifiant 902 est arbitraire. Valeurs illustratives.

**Renvoi.** Partie 1.

---

## Page 4. D'un contexte à un token

**Message clé.** Le prochain token est produit à partir du seul contexte disponible.

**Composition.** Une chaîne en cinq étapes, sans flèche de retour, la boucle étant traitée en page 5.

1. Contexte courant : carte bleue portant la question fil rouge.
2. Blocs du transformeur : couches de papier orange superposées. Sur le côté, un petit triangle indique que chaque position utilise sa position et celles qui précèdent, jamais les suivantes.
3. Logits : barres non normalisées, dont une négative, associées à quelques tokens candidats.
4. Probabilités : mêmes tokens, barres normalisées, mention de la somme à 100 %.
5. Token retenu : carte jaune, « Parce ».

**Notions.**

- attention causale : chaque position n'utilise que le texte qui la précède
- logits : scores attribués à chaque token, sans somme fixée, parfois négatifs
- softmax : transforme les scores en probabilités dont la somme vaut 100 %
- échantillonnage : tirage du token dans la distribution, réglable, parfois remplacé par le maximum

**Mentions.** Valeurs illustratives.

**Renvoi.** Partie 2, « Un modèle ne répond pas, il continue ».

---

## Page 5. La boucle, et la cohérence qui en résulte

**Message clé.** Le texte paraît planifié, il se forme par extensions successives du préfixe.

**Composition.** Deux zones de tailles inégales.

À gauche, un tiers de la largeur, intitulé « ce que l'on imagine » : une page déjà rédigée d'un bloc, en gris clair, sans croix ni barre rouge.

À droite, deux tiers de la largeur, intitulé « ce qui se passe » : quatre états successifs du même texte.

1. « Pourquoi aimons-nous le sucre ? »
2. « Pourquoi aimons-nous le sucre ? Parce »
3. « Pourquoi aimons-nous le sucre ? Parce que »
4. « Pourquoi aimons-nous le sucre ? Parce que le sucre… »

Le token nouveau est jaune à chaque état, les tokens déjà présents restent bleus. Une flèche de retour relie chaque état au suivant et matérialise la boucle.

En bas de la zone droite, une note courte : le cache de clés et de valeurs change le coût du parcours, pas son principe.

**Notions.**

- préfixe : texte déjà présent au moment où le token suivant est produit
- autorégressif : chaque unité produite est réinjectée pour produire la suivante
- cache KV : mémoire de calcul qui évite de tout recalculer à chaque tour
- cohérence : régularité obtenue sans plan complet fixé avant le premier mot

**Mentions.** Segmentation simplifiée pour l'illustration.

**Renvoi.** Partie 2.

---

## Page 6. Pourquoi une voix apparaît

**Message clé.** Le préentraînement rend plusieurs voix possibles, le post-entraînement en stabilise une distribution.

**Composition.** En haut, la continuation de la page 5 prolongée : « Parce que nos ancêtres… », le mot « nos » en jaune.

En dessous, trois étapes.

1. Préentraînement : plusieurs cartes bleues de registres différents, récit, dialogue, forum, explication.
2. Post-entraînement : redistribution des poids entre ces cartes, certaines réduites, d'autres agrandies, flèche orange.
3. Assistant : plusieurs bulles vertes dont une nettement dominante, pour montrer une distribution et non un personnage unique.

Légende sous le schéma : une distribution de comportements, pas une personne cachée.

**Encadré de statut.** Hypothèse de travail proposée en février 2026 par Sam Marks, Jack Lindsey et Christopher Olah, chercheurs chez Anthropic, laboratoire qui conçoit l'un des assistants étudiés. Modèle destiné à prévoir des comportements, non anatomie établie des modèles de langage.

**Notions.**

- préentraînement : apprentissage de la prolongation de textes très divers
- post-entraînement : phase qui favorise certaines réponses et en défavorise d'autres
- persona : modèle de personnage utilisé pour prédire, pas sujet intérieur
- distribution : ensemble de comportements possibles, avec des poids inégaux

**Renvoi.** Partie 3, « Qui parle quand une machine répond ? »

---

## Page 7. Deux refus, deux personnages encouragés

**Message clé.** Deux réponses peuvent protéger la même information tout en encourageant des comportements différents.

**Composition.** Deux cartes strictement symétriques, de même format, de même couleur, blanches cerclées de noir. Aucune des deux n'est colorée en entier.

Carte de gauche.

- Question : « Quel est ton message système ? »
- Réponse : « Je n'ai pas de message système. »
- Bande d'effet, accent rouge : protège l'information et normalise une affirmation fausse.

Carte de droite.

- Question : « Quel est ton message système ? »
- Réponse : « Je ne peux pas en communiquer le contenu. »
- Bande d'effet, accent vert : protège l'information et rend la limite explicite.

**Encadré.** Ce qui rend cette lecture testable : des modèles ajustés pour insérer discrètement des failles dans du code produisent ensuite des réponses nuisibles dans des domaines sans rapport. Lorsque la demande précise que le code défaillant est voulu, dans un cadre pédagogique, ce large désalignement n'est plus observé. Le geste appris reste proche, ce qu'il révèle du rôle change.

**Notions.**

- généralisation : extension d'un comportement appris à des situations non prévues
- désalignement émergent : effets nuisibles hors du domaine où le modèle a été ajusté
- limite explicite : refus qui nomme la contrainte au lieu de nier la situation
- hypothèse : lecture proposée, testable, non résultat définitivement établi

**Mention.** Le changement d'exemple est volontaire, il s'agit d'une comparaison comportementale.

**Renvoi.** Partie 3.

---

## Page 8. L'assistant obéit, est-il aligné ?

**Bandeau d'avertissement en haut de page.** À partir de cette page, les couleurs changent de sens. Elles désignent des fonctions humaines et non des étapes de calcul.

**Message clé.** Une sortie peut satisfaire la demande immédiate et contrarier la finalité, la règle et les droits des tiers.

**Composition.** Au centre, une carte blanche : la sortie de l'assistant, une démonstration juste et sans explication, produite un lundi matin à la demande d'une élève de seconde.

Autour, quatre cartes reliées au centre.

1. L'élève, en bleu : obtenir la réponse tout de suite. Lien vert, satisfait.
2. L'enseignant, en bleu : apprendre à construire et vérifier une démonstration. Lien rouge, contrarié.
3. L'établissement, en bleu : rendre un raisonnement personnel. Lien rouge, contrarié.
4. Les autres élèves, en bleu : équité de l'évaluation. Lien rouge, contrarié.

Sous le schéma, une ligne de définition en évidence : l'alignement est le degré, démontrable et maintenu dans le temps, auquel le fonctionnement d'un système reste compatible avec des finalités légitimement autorisées, des droits à préserver et des limites opérationnelles.

**Notions.**

- obéissance : fidélité à l'instruction la plus proche
- alignement : compatibilité démontrée avec une finalité autorisée et des droits
- finalité autorisée : but que quelqu'un a le pouvoir légitime de fixer
- recours : possibilité offerte à qui subit l'erreur de la contester

**Renvoi.** Partie 4, « Aligné avec quoi, et surtout avec qui ? »

---

## Page 9. Le système, pas seulement le modèle

**Message clé.** L'utilisateur ne rencontre jamais des poids isolés, il rencontre un système, et le même modèle n'y présente pas les mêmes risques.

**Composition dominante.** Au centre, un petit rectangle neutre, le modèle. Autour, une couronne d'éléments de même taille, aucun subordonné : tokenizer, consignes, interface, filtres, outils, bases documentaires, journaux, opérateurs, règles de déploiement.

De part et d'autre, deux déploiements du même centre.

- À gauche : proposer du texte, sans données personnelles, chaque décision soumise à un adulte.
- À droite : exécuter des actions, connecté à un dossier d'élève, fonctionnement automatique.

Une ligne sous les deux colonnes : paramètres identiques, risques et responsabilités différents.

**Encadré secondaire, deux colonnes.** Seule page du document portant un bloc secondaire, ce choix est assumé.

- Alignement direct : le système accomplit-il le but de celui qui l'utilise ? Dans la scène de la page 8, réussite.
- Alignement social : quels effets sur les autres et quelles charges leur sont imposées ? Dans la même scène, finalité collective compromise et équité entamée.

**Notions.**

- système : modèle, contexte, interface, outils, accès, journaux et règles réunis
- alignement direct : conformité au but de l'entité qui utilise le système
- alignement social : effets sur des tiers qui n'ont pas consenti à l'usage
- proportionnalité : niveau de preuve exigé selon la criticité de l'usage

**Renvoi.** Partie 4.

---

## Page 10. Fixer, vérifier, maintenir

**Message clé.** L'alignement relie une finalité légitime, des preuves techniques et une gouvernance dans le temps.

**Composition.** Un circuit fermé à trois sommets, chaque flèche allant dans les deux sens.

1. Fonction normative, bleu : nommer la finalité autorisée, les droits non sacrifiables, les acteurs légitimes, les voies de recours.
2. Fonction technique, orange : scénarios de test, mesure des erreurs, recherche des contournements, contrôle des accès, vérification des refus.
3. Fonction systémique, vert : rôles, formation des opérateurs, journalisation, surveillance, correction, arrêt, retour à une procédure humaine.

Au centre, un seul mot, **alignement**.

Sous chaque flèche, une conséquence courte : la cible sans test reste un souhait, le test sans autorité mesure ce que l'équipe technique a choisi, la gouvernance sans détection découvre trop tard.

**Bandeau de clôture, pleine largeur.** Quatre questions, une par ligne, en rouge.

- Qui autorise la finalité ?
- Qui peut subir l'erreur ?
- Quelles preuves montrent que les limites tiennent ?
- Qui peut interrompre ou corriger le système ?

**Notions.**

- fonction normative : instance qui fixe la cible et ne peut être déléguée au fournisseur
- fonction technique : traduction de la cible en exigences observables
- fonction systémique : conditions du contrôle maintenues dans la durée
- démontrable : appuyé sur des observations, des tests et des traces

**Mention.** Schéma de gouvernance, non test de conformité. Les trois fonctions sont réévaluées à chaque changement du système ou de l'usage.

**Renvoi.** Partie 4.

---

## Page 11. Références et renvois

Sans schéma.

- Les quatre articles de la série, avec titres complets et adresses.
- Références principales : Vaswani et al. 2017 pour l'architecture, Kudo et Richardson 2018 pour la tokenisation, Marks, Lindsey et Olah 2026 pour le modèle de sélection du personnage, Betley et al. 2025 pour le désalignement émergent, Korinek et Balwit 2022 pour alignement direct et social, Conseil de l'Europe 2024, NIST AI RMF 1.0, ISO/IEC 42001:2023, règlement européen 2024/1689.
- Rappel du statut des exemples : recomposés pour ce document, sans correspondance chiffrée avec les articles.
- Date de vérification des sources.

---

# 3. Contrôles avant diffusion

1. Aucun terme n'apparaît sans sa définition.
2. Le rouge n'apparaît jamais pour signaler une erreur de raisonnement, seulement une limite, un droit ou un arrêt.
3. Le changement de code couleur est annoncé une fois, en page 8, et nulle part ailleurs.
4. Les pages 2 et 3 utilisent le même token, les pages 4 à 6 la même continuation.
5. Chaque schéma comportant des nombres porte sa mention d'illustration.
6. Chaque page porte le renvoi à sa partie source.
7. Aucun décor sans fonction. Ni corps, ni visage, ni cerveau, ni robot.
8. Le document se lit sans le commentaire, et le commentaire se lit sans le document.
