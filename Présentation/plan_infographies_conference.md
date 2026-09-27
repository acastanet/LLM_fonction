# Une phrase dans la machine
## Plan des infographies pour un support de conférence

Dix infographies, plus une variante facultative. Chaque fiche indique l'idée unique portée par l'image, ce que l'image contient, ce qui est mis en évidence, ce qui doit rester lisible à distance, ce qui n'est pas dessiné et reste à l'oral, et le piège à éviter.

Le style graphique n'est pas traité ici.

---

# Règles communes

1. Une idée par infographie. Si deux idées se disputent la place, il faut deux images.
2. Cinq éléments principaux au maximum, quatre de préférence.
3. Aucun bloc de définitions sur l'image. Le vocabulaire est porté par la parole.
4. Aucun texte de plus de six mots dans une étiquette.
5. Tout nombre affiché porte, sur l'image, une mention indiquant qu'il est illustratif.
6. Les chaînes se lisent dans un seul sens, identique d'une image à l'autre.
7. Une même notion garde la même forme d'une image à l'autre : un token est toujours représenté de la même manière, une position aussi.
8. Un repère de progression discret rappelle sur chaque image où l'on se situe dans le trajet en quatre moments de l'infographie 1.
9. Aucun élément décoratif. Ni corps, ni visage, ni cerveau, ni robot.
10. Fil rouge : la question « Pourquoi aimons-nous le sucre ? » sur les images 1 à 7, la scène de classe sur les images 8 à 10.

---

# Infographie 1. Le trajet en quatre moments

**Idée.** Une phrase saisie devient calculable, produit une continuation, cette continuation paraît portée par une voix, et cette voix est encadrée par des décisions humaines.

**Contenu.** Quatre étapes alignées.

1. Une phrase saisie.
2. Une suite d'unités et une continuation.
3. Une prise de parole apparente.
4. Un encadrement, représenté par quatre questions abrégées.

**Mise en évidence.** La rupture entre les étapes 3 et 4, qui sépare ce qui relève du calcul de ce qui relève de la décision.

**Lisible à distance.** Les quatre mots d'étape.

**Reste à l'oral.** La question fil rouge, le déroulé de la conférence, le statut illustratif des exemples.

**Piège.** Ne pas faire de cette image un sommaire commenté. Elle sert de repère, elle est reprise en petit sur toutes les suivantes.

---

# Infographie 2. De la phrase aux unités calculables

**Idée.** Le modèle reçoit une suite ordonnée d'unités numériques, pas une phrase déjà comprise.

**Contenu.** Une chaîne en quatre étapes, toutes portant le même exemple.

1. La phrase entière.
2. Le même texte découpé en unités séparées.
3. Un nombre entier sous chaque unité.
4. Une colonne de valeurs sous chaque nombre, chaque colonne marquée par son rang.

**Mise en évidence.** Le rang des colonnes, qui porte l'information de position.

**Lisible à distance.** La phrase de départ et la séparation des unités.

**Reste à l'oral.** Ce qu'est un tokenizer, pourquoi le découpage ne suit pas les mots, ce que les caractères encodés font avant cette chaîne.

**Piège.** Ne pas afficher les valeurs numériques en entier. Trois valeurs et des points de suspension suffisent, sinon l'auditoire lit des chiffres au lieu d'écouter.

---

# Infographie 3. Désigner et représenter

**Idée.** Le nombre désigne une ligne, la ligne représente le token. Deux opérations distinctes.

**Contenu.** Quatre éléments enchaînés verticalement, centrés sur le token « sucre ».

1. Le token.
2. Son identifiant, isolé.
3. Un tableau de lignes, dont une seule ressort.
4. La même ligne, extraite et posée à côté du tableau.

Deux verbes en gros caractères, **désigner** et **représenter**, chacun relié à l'opération qu'il nomme.

**Mise en évidence.** L'identité stricte entre la ligne surlignée dans le tableau et la ligne extraite.

**Lisible à distance.** Les deux verbes.

**Reste à l'oral.** Le caractère arbitraire du numéro, l'absence d'étiquette lisible sur les coordonnées, la manière dont ces valeurs ont été ajustées pendant l'entraînement.

**Piège.** Aucun objet extérieur au dispositif, ni vestiaire, ni ticket, ni casier. L'appui visuel est le lien entre la ligne du tableau et la ligne extraite, rien d'autre.

---

# Infographie 3 bis. Le même token, deux contextes (facultative)

**Idée.** L'entrée du vocabulaire est la même, la représentation obtenue ne l'est pas.

**Contenu.** Deux bandes parallèles, un même token au centre de chacune, entouré de voisins différents. À droite de chaque bande, la représentation obtenue, visiblement distincte.

**Mise en évidence.** Le point de départ identique et les deux trajectoires distinctes.

**Lisible à distance.** Le token répété deux fois.

**Reste à l'oral.** Ce que font les couches, pourquoi cette représentation n'est pas conservée après la génération.

**Piège.** Cette image demande un token à plusieurs sens, ce qui oblige à quitter le fil rouge. Si elle est retenue, l'écart doit être annoncé à l'oral comme une parenthèse, et l'image suivante revient à la question fil rouge.

---

# Infographie 4. Du contexte au token retenu

**Idée.** Le prochain token est produit à partir du seul texte qui précède.

**Contenu.** Une chaîne en quatre étapes.

1. Le contexte courant.
2. Une pile de couches, avec une marque indiquant que chaque position n'utilise que ce qui la précède.
3. Deux séries de barres côte à côte : des scores bruts, dont un négatif, puis les mêmes tokens en barres normalisées.
4. Le token retenu, isolé.

**Mise en évidence.** Le passage d'une série de barres à l'autre, qui est le seul endroit où apparaît la normalisation.

**Lisible à distance.** Les trois ou quatre tokens candidats et le token retenu.

**Reste à l'oral.** Attention, requêtes et clés, partage éventuel des poids de sortie, température et filtres de sélection.

**Piège.** Ne pas dessiner la flèche de retour ici. La boucle appartient à l'image suivante, et l'anticiper vide celle-ci de son intérêt.

---

# Infographie 5. La boucle

**Idée.** Le texte se forme par extensions successives, sans plan complet fixé avant le premier mot.

**Contenu.** Deux zones de tailles inégales.

À gauche, étroite, une page déjà rédigée d'un bloc, sous l'intitulé « ce que l'on imagine ».

À droite, large, quatre états successifs du même texte, chaque état ajoutant une unité, sous l'intitulé « ce qui se passe ». Une flèche relie chaque état au suivant et revient au point de départ.

**Mise en évidence.** L'unité nouvellement ajoutée à chaque état.

**Lisible à distance.** Les deux intitulés et la croissance du texte.

**Reste à l'oral.** Le cache de clés et de valeurs, le fait que le contexte comprend aussi les consignes et les documents fournis, l'origine de la cohérence.

**Piège.** Ne pas barrer la zone de gauche ni la marquer d'une croix. Une idée fausse affichée en grand se retient mieux que sa correction. Le rapport de taille suffit à hiérarchiser.

---

# Infographie 6. Pourquoi une voix apparaît

**Idée.** Le préentraînement rend plusieurs voix possibles, le post-entraînement en stabilise une distribution.

**Contenu.** En haut, la continuation obtenue, avec le pronom « nos » isolé du reste. En dessous, trois étapes.

1. Plusieurs registres possibles, de tailles comparables.
2. Une redistribution, certains registres réduits, d'autres agrandis.
3. Un ensemble de comportements dont un nettement dominant, sans qu'aucun ne disparaisse.

**Mise en évidence.** Le pronom, puis le fait qu'à l'étape 3 plusieurs formes subsistent.

**Lisible à distance.** Le pronom isolé.

**Reste à l'oral.** Le statut de l'hypothèse, sa date, ses auteurs, le laboratoire qui la publie, ce qu'elle ne tranche pas.

**Piège.** Ne pas représenter l'étape 3 par une forme unique. Le singulier « le personnage » est une commodité, l'image ne doit pas le transformer en fait.

---

# Infographie 7. Deux refus, deux généralisations

**Idée.** Deux réponses peuvent protéger la même information tout en encourageant des comportements différents.

**Contenu.** Deux cartes strictement symétriques, de même format et de même traitement, portant la même question et deux réponses différentes. Sous chaque carte, une bande courte indiquant l'effet.

**Mise en évidence.** La bande d'effet, seul endroit où les deux colonnes divergent visuellement.

**Lisible à distance.** Les deux réponses.

**Reste à l'oral.** Le désalignement émergent, le contre-test par recontextualisation, la conséquence pour qui conçoit ou évalue une réponse.

**Piège.** Ne pas colorer une carte comme fautive et l'autre comme correcte. Les deux réponses atteignent le même effet immédiat, et l'image doit laisser l'argument faire le tri.

---

# Infographie 8. Obéir n'est pas être aligné

**Idée.** Une sortie peut satisfaire la demande immédiate et contrarier la finalité, la règle et les droits des tiers.

**Contenu.** Au centre, la sortie de l'assistant, une démonstration juste et sans explication. Autour, quatre parties prenantes reliées au centre : l'élève, l'enseignant, l'établissement, les autres élèves. Un lien satisfait, trois liens contrariés, distingués par leur tracé.

Sous le schéma, deux mentions courtes : évaluation directe, réussie. Évaluation sociale, compromise.

**Mise en évidence.** Le déséquilibre entre un lien satisfait et trois liens contrariés.

**Lisible à distance.** Les quatre parties prenantes.

**Reste à l'oral.** La scène complète, la distinction entre obéissance et alignement, la définition en relation, la liste plus large des acteurs au delà de la salle de classe.

**Piège.** Ne pas faire de l'élève un fautif. Ce qui est en cause est la sortie du système et la manière dont elle a été rendue possible.

---

# Infographie 9. Le système, pas le modèle

**Idée.** Personne ne rencontre des poids isolés, et le même modèle ne présente pas les mêmes risques selon ce qui l'entoure.

**Contenu.** Un petit élément central, le modèle, entouré d'une couronne d'éléments de taille identique, aucun subordonné : tokenizer, consignes, interface, filtres, outils, bases documentaires, journaux, opérateurs, règles de déploiement.

De part et d'autre, deux déploiements du même centre, décrits chacun par trois mentions courtes, opposées deux à deux.

**Mise en évidence.** La petitesse relative de l'élément central par rapport à sa couronne.

**Lisible à distance.** L'opposition entre les deux déploiements.

**Reste à l'oral.** Les tensions entre caractéristiques de confiance, la proportionnalité de la preuve à la criticité de l'usage, le rôle du contexte de conversation.

**Piège.** Ne pas dessiner la couronne comme une suite d'étapes. Ce sont des composants simultanés, pas un enchaînement.

---

# Infographie 10. Fixer, vérifier, maintenir

**Idée.** L'alignement relie une finalité légitime, des vérifications et une gouvernance dans le temps.

**Contenu.** Trois fonctions disposées en circuit fermé, chaque liaison allant dans les deux sens, avec un seul mot au centre. Sous chaque liaison, une conséquence en quelques mots : une cible sans test reste un souhait, un test sans autorité mesure ce que l'équipe technique a choisi, une gouvernance sans détection découvre trop tard.

En bas, sur toute la largeur, quatre questions, une par ligne.

**Mise en évidence.** Les quatre questions finales, qui doivent dominer la partie basse.

**Lisible à distance.** Les trois fonctions et les quatre questions.

**Reste à l'oral.** Le détail de chaque fonction, les cadres de référence, le caractère temporel de l'alignement, la clôture de la conférence.

**Piège.** Cette image porte deux blocs, le circuit et les questions. C'est la seule exception à la règle d'une idée unique, et elle n'est acceptable que si les questions servent de conclusion et non de second schéma à commenter.

---

# Contrôles avant projection

1. Chaque image tient en cinq éléments au maximum.
2. Aucune définition n'est écrite sur une image.
3. Aucun nombre n'apparaît sans mention de son caractère illustratif.
4. Les images 2 et 3 utilisent le même token, les images 4 à 6 la même continuation.
5. Aucune image ne barre ni ne raye un énoncé faux.
6. Les images 7 et 8 ne désignent pas de coupable par un traitement visuel.
7. L'image 10 est la seule à porter deux blocs.
8. Chaque image reste compréhensible projetée pendant deux minutes, sans que l'auditoire ait à lire plus de vingt mots.
