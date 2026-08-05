# Feuille de route — Série « Une phrase dans la machine »

**Version :** 1.2  
**Date :** 4 août 2026  
**Objet :** transformer les quatre brouillons existants en une série cohérente, progressive et publiable sur le fonctionnement des LLM.

**Modifications de la version 1.1 :** la série remplace la collection de fiches existante
(§4) ; le triptyque corpus/entraînement/contexte est réparti entre les parties 2 et 4 (§6
et §8) ; le gabarit commun est instancié section par section (§5 à §8) ; l'expérience du
lancer de pièce retrouve sa place en partie 3 (§7) ; la phrase témoin est déclarée cadre
narratif et non exemple technique (§3) ; le front matter reprend les champs de la chaîne
de publication existante (§13) ; le calendrier passe à douze séances pour doter la
vérification documentaire et le travail graphique (§14).

**Modifications de la version 1.2 :** le guide `styleCVGZ.md` est intégré. Nouveau §10 bis,
qui montre que le gabarit du §10 est déjà la formule du guide, fixe le registre retenu et
règle les huit curseurs article par article ; chaque chantier détaillé (§5 à §8) porte ses
propres réglages ; le vocabulaire du §10 absorbe les termes chargés de valeur et les
registres interdits ; le §15 reçoit un test de la voix et un test des connecteurs.

---

## 1. Résultat attendu

Produire quatre articles autonomes qui répondent ensemble à une seule question :

> **Que se passe-t-il entre la phrase que nous écrivons et la réponse que nous recevons — et où se situent alors la voix, les choix et la responsabilité ?**

La série doit suivre une progression continue :

> **phrase → tokens → vecteurs → représentations contextuelles → probabilités → continuation → voix apparente → alignement et responsabilité**

### Titre de série recommandé

**Une phrase dans la machine**  
*Anatomie d’une réponse de LLM, du texte aux valeurs*

### Public principal retenu

- enseignants, formateurs et cadres de l’éducation ;
- lecteurs cultivés qui utilisent déjà des assistants conversationnels ;
- aucune connaissance préalable en mathématiques ou en apprentissage automatique n’est exigée ;
- les lecteurs plus techniques doivent néanmoins pouvoir reconnaître un mécanisme exact et correctement nuancé.

### Format commun

- 1 600 à 2 100 mots par article, hors encadrés et références ;
- une question principale par article ;
- une distinction conceptuelle structurante ;
- un exemple concret qui traverse le texte ;
- une objection sérieuse ;
- une conclusion qui répond à la question locale et ouvre la suivante ;
- les précisions très techniques sont placées dans des encadrés.

---

## 2. Architecture éditoriale définitive

| Partie | Verbe | Question locale | Distinction centrale | Idée reçue déplacée | Porte de sortie |
|---|---|---|---|---|---|
| 1 | **Entrer** | Que reçoit réellement le modèle ? | mot/token ; identifiant/vecteur ; plongement initial/contextuel | « Le modèle lit des mots. » | À ce stade, aucune réponse n’existe encore. |
| 2 | **Continuer** | Comment le prochain token est-il produit ? | réponse/continuation ; état interne/probabilités | « Le modèle conçoit sa réponse avant de l’écrire. » | Le calcul explique la suite, pas encore la voix. |
| 3 | **Parler** | Pourquoi la continuation paraît-elle avoir une voix ? | observation/interprétation ; personnage/agentivité | « Une voix neutre et unique parle derrière l’écran. » | Choisir un personnage oblige à demander qui choisit. |
| 4 | **Aligner** | Aligné avec quoi, avec qui et sous quelle autorité ? | obéissance/alignement ; direct/social ; modèle/système | « Être aligné signifie obéir à l’utilisateur. » | La finalité reste une responsabilité humaine et institutionnelle. |

### Titres de travail

1. **Comment le texte arrive au modèle ?**  
   *Des unités de langage aux représentations calculables*
2. **Un modèle ne répond pas, il continue**  
   *Du vecteur au prochain token*
3. **Qui parle quand une machine répond ?**  
   *Du mécanisme à la voix apparente*
4. **Aligné avec quoi — et surtout avec qui ?**  
   *Pourquoi l’alignement ne se réduit pas à l’obéissance*

---

## 3. La phrase témoin qui relie les quatre articles

Utiliser, au début ou à la fin de chaque épisode, la même question :

> **Pourquoi aimons-nous le sucre ?**

### Fonction dans chaque partie

| Partie | Usage de la phrase témoin |
|---|---|
| 1 | La phrase apparaît à l’écran, puis elle est découpée, indexée et transformée en représentations numériques. |
| 2 | On suit ses représentations dans les couches jusqu’aux premiers tokens de la continuation. |
| 3 | La réponse produit « nos ancêtres » ou « notre cerveau » : qui est ce « nous » ? |
| 4 | La formule « le personnage que nous voulons » retourne la question : qui est autorisé à parler au nom de ce second « nous » ? |

### Statut de la phrase témoin

La phrase témoin est un **cadre narratif**, non l’exemple technique de chaque article.
Elle est née dans la partie 3, où elle produit réellement « nos ancêtres ». Ailleurs, elle
ouvre et ferme l’épisode sans porter la démonstration. En particulier, elle est un mauvais
exemple de tokenisation : elle ne contient que des formes courantes et n’exhibe aucune
coupure sous-lexicale visible.

Chaque article conserve donc **un** exemple technique propre, déjà présent dans les
sources.

| Partie | Rôle de la phrase témoin | Exemple technique propre |
|---|---|---|
| 1 | ouverture et clôture | *anticonstitutionnellement* pour la tokenisation, *avocat* pour le contexte |
| 2 | rappel de deux lignes | *Le chat noir* pour les colonnes et les couches |
| 3 | cœur de l’article — « nos ancêtres » | le récit Linda–David |
| 4 | retournement du « nous » | l’élève qui réclame la réponse sans explication |

### Règles d’usage

- ne pas refaire toute la démonstration à chaque épisode ;
- rappeler la phrase en deux ou trois lignes au maximum ;
- ne pas forcer la phrase témoin là où l’exemple propre de l’article est plus démonstratif ;
- ne jamais présenter un découpage en tokens comme universel : il dépend du tokenizer et du modèle choisis ;
- si un découpage précis est illustré, indiquer le modèle ou écrire explicitement « exemple simplifié » ;
- utiliser le mot **nous** comme relais narratif entre les parties 3 et 4.

---

## 4. Ordre de travail et priorités

### Décisions déjà tranchées

**La série remplace la collection de fiches existante.** Les sources renvoient à « la fiche
03 », au « tiré à part » et à une « infographie 4:3 » : cette collection avait sa propre
numérotation et son propre format. Elle est close. Conséquences :

- la numérotation en quatre parties devient la seule ; aucun manuscrit ne renvoie plus à un
  numéro de fiche ni au tiré à part ;
- les fichiers sources des fiches sont archivés, jamais écrasés : ils restent des réservoirs ;
- ce qui appartenait au genre de la fiche — récapitulatifs « À retenir », critères de
  travail en deux temps, tableaux autonomes — ne survit que sous forme d’encadré, et une
  seule fois par article (voir §6).

**Le triptyque corpus / entraînement / contexte est réparti entre les parties 2 et 4**
(voir §6 et §8).

### Priorité 0 — Verrouiller les décisions communes

- [ ] Valider le titre de la série.
- [ ] Valider les quatre titres de travail.
- [ ] Valider le public principal.
- [ ] Valider la phrase témoin et son statut de cadre narratif (§3).
- [ ] Décider si les textes seront publiés comme « articles » ou « épisodes » ; employer ensuite le même terme partout. Le mot « fiche » est écarté, la collection étant close.
- [ ] Fixer une longueur cible commune.

**Critère de sortie :** ces six décisions tiennent sur une page et ne sont plus rediscutées pendant la réécriture.

### Priorité 1 — Reconstruire la partie 2

La partie 2 est le principal nœud structurel : deux textes se concurrencent et le fichier de synthèse contient plusieurs versions.

### Priorité 2 — Réécrire la partie 4 dans le genre de la série

Le document actuel est une excellente note de fond, mais pas encore un article destiné au même lecteur.

### Priorité 3 — Raccourcir la partie 1 et nuancer la partie 3

Ces deux textes possèdent déjà leur voix et leur arc principal.

### Priorité 4 — Effectuer la passe transversale

Transitions, terminologie, visuels, références, longueurs et niveau de technicité doivent être harmonisés seulement lorsque les quatre architectures sont stables.

---

## 5. Chantier détaillé — Partie 1

### Sources

- [Version CVGZ principale](<1 _Matrice/Comment_le_texte_arrive_au_modele_texte_fluide_CVGZ.html>)
- [Version antérieure plus courte](<1 _Matrice/Comment le texte arrive au modele.html>)
- illustrations déjà disponibles dans `1 _Matrice`.

### Objectif de l’article

Faire comprendre comment une phrase devient une entrée calculable, sans prétendre que le sens humain est simplement « converti » en nombres.

### Promesse au lecteur

À la fin, le lecteur doit pouvoir expliquer sans confusion la chaîne suivante :

> caractères ou texte encodé → tokens → identifiants → plongements initiaux → entrée ordonnée → représentations contextuelles

### Architecture cible

La dernière colonne renvoie aux neuf temps du gabarit commun (§10). Chaque temps doit
trouver au moins une section : c’est la condition pour que le gabarit soit vérifiable et
non simplement souhaité.

| # | Section | Mots | Contenu | Gabarit |
|---|---|---|---|---|
| 1 | **La phrase à l’écran** | 120-180 | Introduire « Pourquoi aimons-nous le sucre ? » et la différence entre ce que voit le lecteur et ce que reçoit le système. | 1, 2 |
| 2 | **Le modèle ne reçoit pas des mots** | 250-320 | Tokenisation, formes fréquentes ou rares, unité de travail. Exemple propre : *anticonstitutionnellement*. | 3, 4 |
| 3 | **Un numéro qui ne signifie rien** | 180-240 | Identifiant, vestiaire, désignation contre représentation. | 3, 4 |
| 4 | **Le casier contient un vecteur** | 280-350 | Matrice, ligne, coordonnées, calculabilité. | 4 |
| 5 | **Une carte apprise, pas un dictionnaire** | 250-320 | Origine apprise des plongements. **Porte l’unique objection de l’article :** les limites de la métaphore géométrique. | 5, 7 |
| 6 | **Le premier vecteur n’est qu’un départ** | 300-380 | Position, contexte, exemple de l’avocat, entrée vers la partie 2. | 4, 6 |
| 7 | **Ce qu’il faut retenir** | 130-180 | Récapitulation en cinq opérations, une phrase de conséquence pour l’enseignant, transition. | 8, 9 |

La section 7 est brève : la conséquence professionnelle (temps 8) y tient en une ou deux
phrases, pas davantage. La partie 1 n’est pas le lieu des conseils d’usage.

### Réglages de style propres à la partie 1

Curseurs : technicité 2, érudition 1, densité 2, provocation 1 (§10 bis). C’est l’article le
plus technique et le moins référencé de la série.

Connecteur de pivot attribué : « Très bien. Mais », **une seule fois**. Le brouillon actuel
l’emploie deux fois, en section 1 et dans le passage sur les directions de l’espace ; la
seconde occurrence disparaît avec la fusion des sections sur la carte.

Dispositif d’ouverture : la distinction (guide §6.1 D) — ce que voit le lecteur, ce que
reçoit le système.

L’incarnation reste à 3 sans conseil d’usage : elle passe par l’expérience du lecteur, qui
croit que le modèle lit la phrase comme lui.

### À conserver absolument

- « Le token n’est pas une définition du mot. C’est une unité de travail. »
- le ticket de vestiaire et le casier ;
- la distinction désignation/représentation ;
- la distinction plongement initial/représentation contextuelle ;
- « Non pas pour réduire le langage à une mécanique, mais pour comprendre précisément à quel moment la mécanique commence. »

### À raccourcir ou déplacer

- [ ] Réduire les répétitions expliquant que l’identifiant ne possède aucun sens quantitatif.
- [ ] Ramener « D’où viennent les coordonnées ? » à deux ou trois paragraphes.
- [ ] Déplacer la longue section sur la carte dans un encadré.
- [ ] Transformer l’analogie roi–homme+femme en bref repère historique ou la supprimer.
- [ ] Ne pas présenter les directions grammaticales comme une propriété garantie des plongements modernes.
- [ ] Garder un seul véritable passage « On pourrait objecter ».

### À ajouter ou clarifier

- [ ] Si le sous-titre conserve « caractères », ajouter cinq à huit lignes sur l’encodage du texte ; sinon retirer ce terme du sous-titre.
- [ ] Préciser que le tokenizer est généralement un prétraitement distinct du réseau neuronal.
- [ ] Distinguer l’entrée du vocabulaire et ses occurrences dans la phrase.
- [ ] Ajouter une phrase sur la prise en compte de l’ordre ou de la position, sans imposer un mécanisme unique à tous les modèles.
- [ ] Dire qu’un plongement est stable pour un modèle aux paramètres fixés, mais qu’il a été modifié pendant l’entraînement.

### Transition finale à intégrer

> À ce stade, aucune réponse n’existe encore. Nous avons seulement rendu la phrase calculable. Reste à voir comment ces représentations traversent les couches et deviennent une probabilité sur le prochain token.

### Définition de « terminé »

- [ ] Le titre reçoit une réponse directe avant la moitié du texte.
- [ ] La partie ne contient plus un second article autonome sur la géométrie.
- [ ] L’ordre des éléments de la phrase est au moins signalé.
- [ ] Le lecteur peut distinguer token, identifiant et vecteur.
- [ ] La dernière phrase appelle précisément la partie 2.

---

## 6. Chantier détaillé — Partie 2

### Sources

- [Axe narratif et fiche](<2_Traitement/texte synthese.md>)
- [Réservoir technique](<2_Traitement/espace-latent.md>)
- [Schéma existant](<2_Traitement/figure-vecteurs-couches.svg>)

### Décision éditoriale

Créer un nouveau manuscrit propre, sans écraser les sources :

`2_Traitement/article_02_un_modele_continue.md`

Le titre principal sera **Un modèle ne répond pas, il continue**. Le texte `espace-latent.md` ne sera pas publié intégralement comme partie 2 ; il fournira des explications et des encadrés.

### Objectif de l’article

Suivre le trajet d’une séquence dans le transformeur jusqu’au prochain token et montrer qu’une réponse se construit dans une boucle, au lieu d’être rédigée mentalement puis affichée.

### Architecture cible

| # | Section | Mots | Contenu | Gabarit |
|---|---|---|---|---|
| 1 | **Vous écrivez une phrase, le texte se déroule** | 140-200 | Poser l’impression d’une réponse conçue d’avance, puis la contredire. | 1, 2 |
| 2 | **Un vecteur par position** | 250-320 | Reprendre la fin de la partie 1 sans refaire tokenisation et plongement. Exemple propre : *Le chat noir*. | 3 |
| 3 | **Transformer et échanger** | 350-450 | Mouvement propre à chaque position, attention entre positions, progression dans les couches. | 4 |
| 4 | **De l’état interne au vocabulaire** | 300-380 | Dernière position, projection de sortie, logits, softmax. | 4 |
| 5 | **Choisir n’est pas toujours prendre le premier** | 200-260 | Sélection, température et caractère réglable de l’échantillonnage. | 4, 6 |
| 6 | **La boucle** | 220-300 | Le token choisi rejoint la séquence ; la génération recommence. | 6 |
| 7 | **Le plan de câblage n’explique pas la voix** | 180-240 | **Porte l’unique objection de l’article.** Distinguer mécanisme, entraînement, contexte et comportement ; ouvrir la partie 3. | 5, 7, 9 |

Le temps 8 du gabarit — la conséquence humaine ou professionnelle — **n’est pas traité dans
la partie 2**. Il est reporté en partie 4, section 7 (voir ci-dessous et §8).

### Réglages de style propres à la partie 2

Curseurs : technicité 2, érudition 1, densité 2, provocation 1 (§10 bis), identiques à ceux
de la partie 1.

**Point d’attention.** Le brouillon `texte synthese.md` a glissé vers l’essai — son propre
commentaire éditorial le reconnaît ligne 54. Le registre retenu pour la série est le §16.2 du
guide, texte pédagogique : phrases plus courtes, un seul paradoxe principal, termes expliqués
au premier emploi. Le montage doit donc **raccourcir la période** de l’essai, pas seulement
la recopier.

Connecteur de pivot attribué : « Regardons précisément ». La partie 1 ayant « Très bien.
Mais », l’ouverture actuelle du brouillon, qui enchaîne les deux, garde le second et perd le
premier.

Dispositif d’ouverture : le paradoxe (guide §6.1 C) — un texte se déroule, et personne ne
l’a rédigé.

L’incarnation reste à 3 sans conseil d’usage : elle passe par l’expérience du lecteur, qui
croit que quelqu’un a lu et répondu.

### Le sort du triptyque « corpus, entraînement, contexte »

Le meilleur passage disponible dans `texte synthese.md` (l’objection du plan de câblage, le
triptyque, puis « lundi matin, devant une classe… la qualité de ce qui sort est en grande
partie la trace de ce que nous y avons mis ») fait environ 450 mots. La section 7 lui en
accorde 240 au maximum, et la partie 2 ne doit pas s’achever sur des conseils d’usage. Le
passage est donc coupé en deux.

- **Reste en partie 2, section 7 :** l’objection et le triptyque seuls, environ 200 mots. Le
  triptyque y sert de rampe vers la partie 3, qui traite justement du préentraînement puis
  du post-entraînement.
- **Part en partie 4, section 7 :** « notre prise » et « lundi matin devant une classe ». Le
  passage y rime avec la formule de clôture de la série — ce que nous ne pouvons pas
  déléguer, c’est précisément ce que nous avons placé dans le contexte et dont nous devons
  répondre.
- **Disparaît :** le critère de travail en deux temps (`texte synthese.md`, lignes 101-104)
  et le bloc « À retenir » (lignes 106-112). Ils appartenaient au genre de la fiche, désormais
  clos (§4). Le critère peut reparaître, réécrit, dans le passage déplacé en partie 4.

### Montage précis des deux brouillons

- [ ] Reprendre l’ouverture de l’essai présent dans `texte synthese.md` (lignes 34-40).
- [ ] Supprimer du manuscrit final les commentaires éditoriaux placés avant le titre (lignes 1-29) et après l’essai (lignes 52-54, 116-120).
- [ ] Ne conserver que la version en texte courant de la chaîne, jamais les deux.
- [ ] Placer le tableau en six opérations en **encadré récapitulatif unique**, à la fin, et ne pas y rappeler ce que le corps du texte a déjà dit.
- [ ] Écarter le bloc « À retenir » et le critère de travail en deux temps (collection de fiches close, §4).
- [ ] Retirer toute mention de « la fiche 03 », du « tiré à part » et de l’« infographie 4:3 » ; les remplacer par un rappel de la partie 1 en deux lignes.
- [ ] Reprendre de `espace-latent.md` la section « Ce qui traverse les couches ».
- [ ] Reprendre l’encart « De l’état interne au token choisi », après révision.
- [ ] Garder le schéma des colonnes et des couches.
- [ ] Réduire « Avocat, de nouveau » à deux phrases de rappel.
- [ ] Transformer « Faut-il vraiment parler d’espace latent ? » en encadré terminologique facultatif.
- [ ] Couper la section 7 de l’essai selon la règle ci-dessus : objection et triptyque restent, « notre prise » et « lundi matin » partent en partie 4.

### Répétitions à supprimer

- tokenisation ;
- définition générale de la matrice de plongement ;
- métaphore complète de la carte ;
- longue explication du mot « avocat » ;
- origine des plongements ;
- analogie roi–reine.

Ces éléments appartiennent à la partie 1. La partie 2 commence au moment où les vecteurs sont déjà entrés dans le calcul.

### Points de précision à vérifier

- [ ] Ne pas confondre l’espace mathématique continu et le nuage fini des vecteurs du vocabulaire.
- [ ] Ne pas dire que toutes les dimensions internes restent identiques à chaque opération ; parler du flux principal lorsque c’est ce qui est visé.
- [ ] Remplacer « rien n’est fusionné » par « la séquence n’est pas réduite à un vecteur unique, même si l’attention mélange les informations ».
- [ ] Ne pas présenter l’information de position comme nécessairement ajoutée une seule fois avant la première couche.
- [ ] Dire qu’une position causale peut généralement consulter sa propre position et les précédentes.
- [ ] Dire que les activations ne sont pas stockées dans les paramètres et ne persistent normalement pas après le calcul.
- [ ] Présenter le nouveau parcours comme une boucle conceptuelle ; signaler en encadré que des caches évitent de tout recalculer en production.
- [ ] Remplacer « tout jugement relève du contexte » par une formulation reconnaissant le rôle du corpus et de l’entraînement.

### Transition finale à intégrer

> Nous savons désormais comment une suite apparaît : les représentations se transforment, la dernière position est confrontée au vocabulaire, puis un token est choisi. Mais ce trajet n’explique pas pourquoi la continuation dit parfois « nos ancêtres », ni pourquoi elle se montre prudente ou péremptoire. Le calcul explique comment la suite apparaît ; il reste à comprendre qui semble parler.

### Définition de « terminé »

- [ ] Il ne reste qu’un seul manuscrit continu.
- [ ] La boucle est plus visible que la liste des composants.
- [ ] La partie 1 n’est résumée qu’en un paragraphe.
- [ ] Le lecteur sait distinguer état interne, logits, probabilités et token choisi.
- [ ] Le texte s’arrête sur la question de la voix, pas sur un cours de prompting.
- [ ] Le tableau en six opérations apparaît une seule fois, en encadré, et le corps du texte ne le redouble pas.
- [ ] Aucune trace de l’ancienne collection de fiches ne subsiste.

---

## 7. Chantier détaillé — Partie 3

### Source

- [Texte actuel](<3_Qui parle/qui-parle-quand-une-machine-repond.md>)
- [Illustration](<3_Qui parle/psm.png>)

### Précaution de version

Le front matter indique `status: published`. Ne pas remplacer silencieusement une version déjà publiée. Créer au besoin :

`3_Qui parle/article_03_qui_parle_version_serie.md`

### Objectif de l’article

Montrer comment une continuation statistique peut prendre la cohérence apparente d’une voix, en présentant le modèle de sélection du personnage comme une hypothèse féconde, non comme la description définitivement établie de tous les assistants.

### Architecture cible

| # | Section | Contenu | Gabarit |
|---|---|---|---|
| 1 | **Une phrase de trop : « nos ancêtres »** | Conserver presque intact. | 1 |
| 2 | **Ce que prédire exige** | Préentraînement et multiplicité des voix. Exemple propre : le récit Linda–David. | 2, 4 |
| 3 | **L’hypothèse du personnage** | Post-entraînement comme sélection ou stabilisation. | 3 |
| 4 | **Les expériences qui soutiennent cette lecture** | Code défaillant et contre-test. | 4 |
| 5 | **Ce que cette hypothèse change techniquement** | Refus honnête contre mensonge protecteur. **Porte la conséquence professionnelle.** | 6, 8 |
| 6 | **Ce qu’elle ne tranche pas** | Masque, décor, aiguilleur, expérience du lancer de pièce, agentivité. **Porte l’objection.** | 5, 7 |
| 7 | **Aligner quel personnage ?** | Conclusion et transition. | 9 |

### L’expérience du lancer de pièce doit revenir

Elle figure dans le texte actuel (lignes 121-129) et n’apparaissait dans aucune architecture
antérieure. Elle est pourtant le seul élément qui **départage** les trois positions : les
préférences du modèle débordent dans une voix qui n’est pas la sienne, ce qu’un décor sans
volonté propre ne ferait pas. C’est aussi le seul résultat que les auteurs publient contre
leur propre thèse, ce qui fonde l’honnêteté de la note.

**Emplacement :** section 6, après la présentation des trois positions, avec la conclusion
« la plus simple des trois s’en trouve fragilisée ». Ne pas la traiter comme une preuve
décisive : elle déplace un équilibre, elle ne clôt pas la question.

### Réglages de style propres à la partie 3

Curseurs : érudition 3, densité 3, provocation 2, technicité 1 (§10 bis). Le registre
pédagogique est complété ici par le §16.4 du guide, note de recherche : oralité réduite,
objection et limite méthodologique obligatoires, incertitudes explicites.

**Autorisation de vocabulaire.** La partie 3 est la seule à pouvoir employer « âme »,
« vouloir » ou « personnage » dans leur sens plein, parce que son sujet est précisément
l’anthropomorphisme (guide §8.3). L’autorisation ne dispense de rien : chaque emploi
indique de quel niveau il parle. Le test de l’anthropomorphisme (§15) ne s’applique donc pas
mécaniquement à cet article.

Connecteur de pivot attribué : « On pourrait objecter ». Dispositif d’ouverture : l’anecdote
troublante, déjà en place avec « nos ancêtres ».

### Trois niveaux épistémiques à signaler

Employer des formulations ou des intertitres qui séparent clairement :

1. **Observation :** des assistants emploient des formulations et manifestent des comportements anthropomorphiques inattendus.
2. **Interprétation proposée :** le modèle de sélection du personnage cherche à expliquer ces régularités.
3. **Question ouverte :** cette interprétation ne détermine pas où attribuer buts, préférences ou agentivité.

### Formulations à réviser

- [ ] « apprend nécessairement à simuler » → formulation moins absolue ;
- [ ] « Personne n’a appris cela à la machine » → « aucune consigne explicite ne le demandait » ;
- [ ] « ce qui exclut la recopie » → « ce qui rend peu plausible une simple phrase fixe recopiée » ;
- [ ] « Le second entraînement fonctionne ainsi » → préciser qu’il s’agit du modèle interprétatif proposé ;
- [ ] « Aucune théorie n’explique » → « cette hypothèse l’explique de manière particulièrement simple » ;
- [ ] « capacité à vouloir » → distinguer conduite orientée vers un but, préférence apprise et volonté subjective ;
- [ ] « preuves solides » → choisir entre « résultats convergents », « indices expérimentaux » ou une justification plus précise ;
- [ ] « Nous savons désormais » → conserver une conclusion proportionnée aux résultats présentés.

### Coupes

- [ ] Conserver « En bref » seulement s’il sert de chapeau éditorial sur le site.
- [ ] Éviter que « En bref », « La règle », « Retour au sucre » et « Ce qui reste acquis » résument quatre fois la même thèse.
- [ ] Raccourcir le passage bayésien si l’article dépasse la longueur cible.
- [ ] Garder les trois images masque/décor/aiguilleur, mais rappeler qu’elles sont des modèles explicatifs.

### Transition finale à intégrer

> Mais « le personnage que nous voulons » laisse deux mots sans réponse : qui est ce « nous », et que voulons-nous lui faire respecter ? Quelles valeurs doivent limiter ses réponses, qui les choisit et comment vérifier qu’elles tiennent dans une situation nouvelle ? C’est le problème de l’alignement.

### Définition de « terminé »

- [ ] Le lecteur sait à tout moment ce qui est observé, interprété ou encore ouvert.
- [ ] Le modèle du personnage n’est jamais présenté comme un personnage littéralement rangé dans une région du réseau.
- [ ] Les répétitions finales ont été réduites.
- [ ] L’expérience du lancer de pièce figure en section 6 et sert à départager les trois positions.
- [ ] La conclusion pose explicitement les questions « qui choisit ? » et « selon quelles valeurs ? ».

---

## 8. Chantier détaillé — Partie 4

### Source

- [Note de fond actuelle](<4_Alignement/definition explication.md>)
- `4_Alignement/Mission-Alignement-IA-Rapport-DEF.pdf`, à utiliser comme source et non comme modèle de ton.

### Décision éditoriale

Ne pas corriger le document actuel paragraphe par paragraphe. Créer un nouvel article :

`4_Alignement/article_04_aligne_avec_qui.md`

La note actuelle reste le réservoir conceptuel et bibliographique.

### Objectif de l’article

Faire comprendre que l’alignement n’est ni la docilité d’une machine, ni une qualité morale intérieure, ni une certification obtenue une fois pour toutes. Il s’agit d’une relation entre un système, une finalité autorisée, des droits, des limites, un contexte et des acteurs légitimes.

### Scène d’ouverture recommandée

> Un élève demande à un assistant : « Donne-moi directement la réponse, sans explication. » L’assistant obéit parfaitement. Est-il aligné ? Avec la demande immédiate de l’élève, peut-être. Avec la finalité de l’apprentissage, pas nécessairement.

Cette scène doit faire naître la distinction centrale :

> **Obéir à une instruction n’est pas encore être aligné.**

**Risque à traiter avant rédaction.** Le guide de style emploie l’exemple de l’élève trois
fois pour démontrer sa propre méthode : au §12, l’élève qui obtient une démonstration sans
pouvoir l’expliquer ; au §13.2, l’IA qui aide l’élève ; au §14, la machine qui deviendrait
un maître. La scène retenue ci-dessus en est très proche, et le §18 point 11 du guide
interdit d’imiter les formulations des sources.

La scène doit donc être **spécifiée** pour cesser d’être l’exemple générique du guide :
une discipline nommée, un exercice précis, un moment de l’année, un enjeu daté. Une scène
qui pourrait figurer telle quelle dans `styleCVGZ.md` est une scène à réécrire.

### Réglages de style propres à la partie 4

Curseurs : érudition 3, densité 3, provocation 2, fermeté 3, technicité 1 (§10 bis). C’est
le seul article dont la fermeté de conclusion monte à 3 : il tranche pour toute la série.

Le registre pédagogique demande une conclusion **sous forme de critère**, non de formule. La
formule de clôture retenue plus bas est conservée, mais elle doit être précédée du critère :
à qui la question se pose, et à quel moment elle doit être posée.

Connecteur de pivot attribué : « Il faut distinguer ». Dispositif d’ouverture : l’anecdote
troublante.

### Architecture cible

| # | Section | Mots | Contenu | Gabarit |
|---|---|---|---|---|
| 1 | **L’assistant obéit. Est-ce suffisant ?** | 180-240 | Cas de l’élève, contradiction entre demande et finalité. | 1, 2 |
| 2 | **Aligné avec quoi et avec qui ?** | 250-320 | Utilisateur, enseignant, institution, droit, personnes concernées. | 3 |
| 3 | **Une relation, pas une vertu de la machine** | 220-280 | Définition simple, graduelle et contextuelle. | 3, 6 |
| 4 | **Alignement direct et alignement social** | 300-380 | Accomplir la tâche ; préserver les droits et les finalités qui la limitent. | 4 |
| 5 | **Le système, pas seulement le modèle** | 260-340 | Modèle, consignes, outils, données, opérateurs et conditions de déploiement. **Porte l’objection :** « il suffirait d’aligner le modèle ». | 4, 5 |
| 6 | **Fixer, vérifier, maintenir** | 300-380 | Normatif, technique et systémique sous forme d’une chaîne de responsabilité. | 6, 7 |
| 7 | **Ce que nous ne pouvons pas déléguer** | 280-340 | Conclusion de l’article et de la série. **Reçoit le passage déplacé de la partie 2** : « notre prise » et « lundi matin devant une classe ». | 8, 9 |

**Total : 1 790 à 2 280 mots.** La section 7 a été portée de 180-240 à 280-340 mots pour
absorber la conséquence professionnelle de la série entière (§6). C’est la seule fourchette
qui dépasse légèrement la cible commune ; le dépassement est assumé, la conclusion ferme
quatre articles et non un seul.

### Le passage déplacé depuis la partie 2

À réécrire, non à recopier. Ce qu’il doit conserver :

- notre prise directe se situe dans le contexte, et dans une moindre mesure dans les
  réglages de sélection ; ni le corpus ni l’entraînement ne sont à notre portée ;
- cette marge est étroite et sérieuse à la fois : aucune formulation habile ne remplace un
  entraînement, mais tout ce qui paraît relever du jugement de la machine relève d’un
  contexte que quelqu’un a écrit ;
- la conséquence : la qualité de ce qui sort de l’outil est en grande partie la trace de ce
  que nous y avons mis.

Ce qu’il doit gagner en partie 4 : le passage n’est plus un conseil d’usage, il devient la
démonstration que la responsabilité n’est pas déductible du calcul. Le « nous » qui écrit le
contexte est le même « nous » que la partie 3 avait laissé sans réponse.

### Idées de la note actuelle à conserver

- l’alignement est une relation, non une qualité morale de la machine ;
- il est graduel, contextuel, démontrable et maintenu dans le temps ;
- il porte sur le système sociotechnique, pas seulement sur le modèle ;
- il faut distinguer alignement direct et alignement social ;
- le normatif fixe la cible, le technique l’éprouve, le systémique maintient les conditions de contrôle ;
- l’alignement ne se confond ni avec l’obéissance, ni avec la conformité documentaire, ni avec le risque nul.

### Ce qui doit disparaître du corps principal

- [ ] toutes les mentions non expliquées à « la définition retenue dans le rapport » ;
- [ ] l’évaluation détaillée d’une définition antérieure ;
- [ ] la succession de deux définitions longues et quasi juridiques ;
- [ ] l’accumulation de références institutionnelles dans chaque paragraphe ;
- [ ] les développements conçus comme recommandations de rédaction pour un rapport ;
- [ ] le titre « Proposition de définition de l’alignement ».

Les références peuvent être regroupées dans une section finale « Pour aller plus loin » ou dans des notes.

### Conclusion de série visée

La conclusion doit revenir au trajet commencé dans la partie 1 :

- la phrase n’entre jamais telle quelle dans le modèle ;
- la réponse n’est jamais conçue d’un bloc ;
- la voix n’est pas celle d’un sujet simplement caché dans la machine ;
- les finalités et les limites ne peuvent pas être déduites du calcul seul.

Formule de travail :

> Nous pouvons déléguer une partie du calcul, de la recherche et de la formulation. Nous ne pouvons pas déléguer silencieusement la décision de ce que la réponse doit servir, de ce qu’elle ne doit pas sacrifier et de qui devra en répondre.

### Définition de « terminé »

- [ ] L’article commence par une situation, pas par une définition institutionnelle.
- [ ] La distinction obéissance/alignement structure tout le texte.
- [ ] « Avec qui ? » reçoit une réponse plurielle et concrète.
- [ ] Les trois branches ne deviennent pas trois mini-rapports.
- [ ] Le passage venu de la partie 2 est réécrit, non recopié, et sert la responsabilité plutôt que le conseil d’usage.
- [ ] La conclusion ferme les quatre épisodes, pas seulement la partie 4.

---

## 9. Transitions officielles de la série

Ces transitions constituent le passage de relais. Elles doivent rester stables pendant la réécriture.

### Partie 1 → Partie 2

> À ce stade, aucune réponse n’existe encore. Nous avons seulement rendu la phrase calculable. Reste à voir comment ces représentations traversent les couches et deviennent une probabilité sur le prochain token.

### Partie 2 → Partie 3

> Nous savons désormais comment une suite apparaît : les représentations se transforment, la dernière position est confrontée au vocabulaire, puis un token est choisi. Mais ce trajet n’explique pas pourquoi la continuation dit parfois « nos ancêtres », ni pourquoi elle se montre prudente ou péremptoire. Le calcul explique comment la suite apparaît ; il reste à comprendre qui semble parler.

### Partie 3 → Partie 4

> Mais « le personnage que nous voulons » laisse deux mots sans réponse : qui est ce « nous », et que voulons-nous lui faire respecter ? Quelles valeurs doivent limiter ses réponses, qui les choisit et comment vérifier qu’elles tiennent dans une situation nouvelle ? C’est le problème de l’alignement.

---

## 10. Harmonisation transversale

### Gabarit commun de chaque article

1. une scène, une question ou une anomalie ;
2. l’intuition spontanée du lecteur ;
3. une distinction qui déplace cette intuition ;
4. le mécanisme, le cas ou l’expérience ;
5. une objection réelle ;
6. ce que l’explication permet d’affirmer ;
7. ce qu’elle ne permet pas d’affirmer ;
8. une conséquence humaine ou professionnelle ;
9. la question suivante.

Ces neuf temps ne sont pas neuf sections. Chacune des quatre architectures cibles (§5 à §8)
porte une colonne **Gabarit** qui indique quelle section assume quel temps. Un temps sans
section attribuée est un temps qui ne sera pas écrit.

**Récapitulatif des deux temps les plus souvent oubliés :**

| Partie | Temps 5 — l’objection | Temps 8 — la conséquence humaine |
|---|---|---|
| 1 | section 5, limites de la métaphore géométrique | section 7, une à deux phrases |
| 2 | section 7, le plan de câblage | reporté en partie 4 |
| 3 | section 6, ce qu’elle ne tranche pas | section 5, refus honnête contre mensonge protecteur |
| 4 | section 5, « il suffirait d’aligner le modèle » | section 7, passage venu de la partie 2 |

Une seule objection par article, réelle et développée : c’est la règle du §10 sur le ton, et
la colonne du tableau en est l’application.

### Vocabulaire stable

| Employer | Réserver ou expliciter |
|---|---|
| token, identifiant, vecteur, plongement initial, représentation contextuelle | « mot » lorsqu’il désigne en réalité un token |
| couche ou bloc de transformeur | « étage », utilisé seulement comme image annoncée |
| attention entre positions | « le modèle regarde », qui reste une commodité de langage |
| état interne ou activation | « pensée », « idée intérieure » |
| logits, puis probabilités | « probabilités » avant la softmax |
| sélection ou échantillonnage | « le modèle choisit » sans précision |
| comportement orienté vers un but | volonté subjective ou désir |
| système d’IA | modèle, lorsque les outils, règles et opérateurs sont aussi concernés |

### Termes chargés de valeur

Le tableau ci-dessus règle les termes techniques. Le §8.3 du guide règle ceux qui portent un
jugement, et il n’en dispense aucun.

| Employer | Réserver ou expliciter |
|---|---|
| un régime de vérité précisé | « vérité » sans qualificatif |
| une performance mesurée | « intelligence » attribuée à la machine |
| un critère explicite | « créativité » |
| une capacité décrite | « humain » employé comme généralité morale |
| — | « âme » : **autorisé dans la partie 3 seulement**, qui interroge explicitement l’anthropomorphisme |

L’exception de la partie 3 est écrite ici pour que le test de l’anthropomorphisme (§15) ne
signale pas à tort un article dont le sujet **est** l’anthropomorphisme.

### Registres interdits

Guide §8.4. Aucun de ces deux registres n’apparaît dans la série.

- **Managérial ou promotionnel :** disruption, solution révolutionnaire, expérience fluide,
  optimisation sans friction, potentiel illimité, changement de paradigme non défini,
  synergie, game changer, « augmenter l’humain » sans dire ce qui est diminué.
- **Cliché anti-IA :** « la machine est froide », « l’humain a des émotions, donc il
  gagnera », « l’IA ne sera jamais créative », « tout outil est neutre ».

La règle du guide tient en une phrase : la série exige un raisonnement, pas un slogan.

### Règles de ton

- une seule métaphore dominante par section ;
- toute métaphore technique est suivie du terme exact ;
- une objection forte par article vaut mieux que plusieurs objections décoratives ;
- une occurrence par article au maximum pour chaque connecteur signature, selon la
  répartition du §10 bis ;
- une pointe d’humour concret par article au maximum ;
- ne pas employer « comprendre », « vouloir », « décider » ou « savoir » sans préciser le niveau décrit ;
- distinguer systématiquement fait, simplification pédagogique, hypothèse et question ouverte ;
- une référence non expliquée est supprimée, jamais conservée comme signe de sérieux
  (guide §3.3) ;
- trois noms propres par paragraphe au maximum (guide §15.2).

### Chapeau commun à ajouter

Chaque article doit commencer par :

> **Une phrase dans la machine — Partie X/4.** Dans l’épisode précédent… Dans celui-ci, nous suivons…

Le rappel de l’épisode précédent ne doit pas dépasser 50 mots.

---

## 10 bis. Réglages de style

Référence : `styleCVGZ.md`, v1.0. Ce guide n’est pas un document de travail, il ne se
modifie pas. La présente section indique comment la série l’applique.

### Le style est déjà dans la structure

Le gabarit en neuf temps du §10 **est** la formule générale du §2 du guide, à un
dédoublement près. Il n’y a donc pas de couche de style à ajouter par-dessus l’architecture :
respecter le gabarit, c’est déjà écrire dans cette voix.

| Guide §2 — formule générale | Feuille de route §10 — gabarit |
|---|---|
| 1. Une question réelle | 1. une scène, une question ou une anomalie |
| 2. Une difficulté ou un trouble | 2. l’intuition spontanée du lecteur |
| 3. Une distinction conceptuelle | 3. une distinction qui déplace cette intuition |
| 4. Un détour savant | 4. le mécanisme, le cas ou l’expérience |
| 5. Une objection | 5. une objection réelle |
| 6. Un retournement | 6. ce que l’explication permet d’affirmer |
| — | 7. ce qu’elle ne permet pas d’affirmer |
| 7. Une incarnation | 8. une conséquence humaine ou professionnelle |
| 8. Une conclusion ouverte mais ferme | 9. la question suivante |

Le seul écart, le dédoublement du retournement, est ce que le §16.4 du guide exige d’une
note de recherche : incertitudes explicites et limite méthodologique obligatoire. La série
est donc légèrement plus prudente que le guide, jamais moins.

### Registre retenu

**§16.2 du guide — texte pédagogique.** Le public déclaré n’exige aucune connaissance
préalable. Quatre conséquences opposables pendant la réécriture :

- les termes techniques sont expliqués **au premier emploi**, jamais renvoyés à plus loin ;
- les phrases sont plus courtes que dans le brouillon actuel de la partie 2, qui a glissé
  vers l’essai ;
- **un seul paradoxe principal par article** : celui de la colonne « idée reçue déplacée »
  du §2, pas un autre ;
- la conclusion prend la forme d’une **action ou d’un critère**, non d’une formule.

Ce dernier point vise la partie 4. Sa formule de clôture est conservée, mais elle doit être
précédée d’un critère utilisable : à qui la question se pose, et à quel moment.

**La partie 3 emprunte en outre au §16.4**, note de recherche : oralité réduite, objection
et limite méthodologique obligatoires. Son front matter porte déjà `type: note`.

### Les huit curseurs, article par article

Le registre tient la voix ; les curseurs du §17 du guide tiennent la densité. Échelle de 0 à 3.

| Paramètre | Défaut | P1 Entrer | P2 Continuer | P3 Parler | P4 Aligner |
|---|---:|---:|---:|---:|---:|
| Oralité | 2 | 2 | 2 | 2 | 2 |
| Érudition | 2 | 1 | 1 | 3 | 3 |
| Densité conceptuelle | 2 | 2 | 2 | 3 | 3 |
| Humour | 1 | 1 | 1 | 1 | 1 |
| Provocation | 1 | 1 | 1 | 2 | 2 |
| Incarnation | 3 | 3 | 3 | 3 | 3 |
| Technicité | 1-2 | 2 | 2 | 1 | 1 |
| Fermeté de conclusion | 2 | 2 | 2 | 2 | 3 |

Les parties 1 et 2 portent la technique et peu de références ; les parties 3 et 4 portent les
références et la densité conceptuelle ; la fermeté monte au dernier article, qui tranche pour
toute la série.

### L’incarnation n’est pas le conseil d’usage

L’incarnation est le seul curseur à 3, et elle le reste dans les quatre parties, alors même
que les parties 1 et 2 ne portent pas le temps 8 du gabarit. Ce n’est pas une contradiction :
le guide sépare lui-même deux figures.

| Figure du guide | Ce qu’elle fait | Où |
|---|---|---|
| §11.6 — le détail matériel | Ancre l’abstrait dans une situation vécue. « Vous lisez cette phrase et vous croyez que le modèle la lit aussi. » | Partout, curseur à 3 |
| §11.3 — le retour au concret | Tire la conséquence professionnelle. « Lundi matin, un élève devra tout de même décider. » | Partie 4 seulement, temps 8 |

Un texte peut donc être incarné de bout en bout sans donner un seul conseil. « Lundi matin
devant une classe » est une instance littérale de la figure §11.3 : c’est une figure de
signature, elle s’use si on l’emploie deux fois. Elle est réservée à la conclusion de la
partie 4.

### Quota et répartition des connecteurs signature

Mesure faite sur les brouillons : **« Très bien. Mais » apparaît deux fois dans la partie 1
et une fois dans la partie 2**, toujours au même endroit du raisonnement, le pivot après
l’intuition naïve. Le §7.4 du guide encourage ces connecteurs ; leur répétition les tue.

**Règle : une occurrence par article au maximum** pour « Très bien. Mais », « Il faut
distinguer », « On pourrait objecter », « Prenons un exemple », « Regardons précisément »
et « Voilà ».

**Deux articles consécutifs n’ouvrent pas sur le même geste.** Répartition retenue, d’après
les quatre dispositifs d’ouverture du §6.1 du guide :

| Partie | Dispositif d’ouverture | Connecteur de pivot |
|---|---|---|
| 1 | D — la distinction | « Très bien. Mais » |
| 2 | C — le paradoxe : le texte se déroule, personne ne l’a rédigé | « Regardons précisément » |
| 3 | A — l’anecdote troublante : « nos ancêtres » | « On pourrait objecter » |
| 4 | A — l’anecdote troublante : l’élève | « Il faut distinguer » |

Les parties 3 et 4 ouvrent toutes deux sur une anecdote, ce qui est acceptable : les scènes
sont de nature opposée, une bizarrerie observée et une demande légitime.

---

## 11. Vérification technique et documentaire

Effectuer cette passe après la réécriture structurelle, pas avant.

### Partie 1

- [ ] encodage, tokenisation et frontière du modèle ;
- [ ] identifiant de vocabulaire contre occurrence ;
- [ ] plongement d’entrée contre représentation contextuelle ;
- [ ] prise en compte de la position ;
- [ ] statut historique et limites des analogies vectorielles.

### Partie 2

- [ ] attention causale et circulation entre positions ;
- [ ] flux principal contre dimensions intermédiaires ;
- [ ] dernière position utilisée pour la génération ;
- [ ] projection de sortie, logits, softmax ;
- [ ] matrice d’entrée éventuellement réutilisée en sortie, sans présenter ce choix comme universel ;
- [ ] température, filtres et échantillonnage ;
- [ ] différence entre boucle conceptuelle et calcul optimisé par cache.

### Partie 3

- [ ] référence exacte du texte étudié ;
- [ ] séparation entre résultats expérimentaux et interprétation proposée ;
- [ ] description fidèle des deux expériences ;
- [ ] prudence sur la généralisation à tous les modèles ;
- [ ] définition non psychologique de l’agentivité, sauf discussion explicite.

### Partie 4

- [ ] définition stable de l’alignement ;
- [ ] distinction alignement/conformité ;
- [ ] distinction alignement direct/social ;
- [ ] distinction modèle/système ;
- [ ] références juridiques et institutionnelles à jour ;
- [ ] chaque source soutient précisément la proposition à laquelle elle est attachée ;
- [ ] **les huit URL de `definition explication.md` ouvertes une à une**, paramètre
  `?utm_source=chatgpt.com` retiré : RIA, NIST AI RMF (deux pages), ISO/IEC 42001,
  Convention-cadre du Conseil de l’Europe, International AI Safety Report 2026, NBER,
  Springer, arXiv ;
- [ ] **les quatre appels de note orphelins vers le rapport PDF** (`definition explication.md`
  lignes 13, 17, 112 et 128, où la référence n’a pas survécu à la copie) remplacés par des
  renvois de page vérifiables, ou supprimés avec la phrase qu’ils prétendaient soutenir.

### Règle de preuve

Pour toute affirmation technique ou expérimentale importante :

1. privilégier une publication scientifique, la documentation officielle ou la source primaire ;
2. éviter qu’une illustration pédagogique soit présentée comme une mesure réelle ;
3. dater les données susceptibles d’évoluer ;
4. signaler explicitement ce qui dépend du modèle ou de l’architecture ;
5. conserver une liste des vérifications dans un fichier séparé si nécessaire.

---

## 12. Plan des visuels

| Partie | Visuel principal | Message unique | Action |
|---|---|---|---|
| 1 | texte → tokens → identifiants → lignes de matrice | une phrase doit devenir calculable | Choisir ou adapter une illustration existante. |
| 2 | colonnes, couches, sortie et flèche de retour | la génération est une boucle | Réviser `figure-vecteurs-couches.svg` en ajoutant clairement la sortie et le retour. |
| 3 | réserve de voix → post-entraînement → personnage de l’assistant | une voix est stabilisée parmi plusieurs possibles | Vérifier que `psm.png` ne transforme pas l’hypothèse en localisation littérale. |
| 4 | cible légitime → moyens techniques → maintien systémique | l’alignement relie norme, comportement et gouvernance | Créer un schéma simple, pas une infographie juridique exhaustive. |

### Deux fonctions à ne pas mélanger

Le dossier `1 _Matrice` contient deux familles d’images : des illustrations générées, larges
et atmosphériques, et des schémas explicatifs comme `figure-vecteurs-couches.svg`. Les règles
communes ci-dessous ne s’appliquent qu’aux seconds.

- **Schéma explicatif** — un par partie, obligatoire, il porte le mécanisme. Palette,
  typographie et ratio communs aux quatre.
- **Illustration d’ouverture** — facultative, elle ne démontre rien et ne doit jamais être
  légendée comme si elle décrivait le fonctionnement du modèle.

Décider en séance 10 si les illustrations générées sont conservées. Si elles le sont, elles
n’entrent pas dans la contrainte d’homogénéité graphique des schémas, mais leur légende doit
signaler qu’elles sont décoratives.

### Règles graphiques communes aux quatre schémas

- même ratio et mêmes marges ;
- même palette ;
- même typographie ;
- une légende qui indique ce qui est réel, simplifié ou métaphorique ;
- pas plus de sept éléments principaux par visuel ;
- le visuel doit rester compréhensible sans le texte, et le texte sans le visuel.

---

## 13. Organisation recommandée des fichiers

Ne pas écraser les documents sources pendant la restructuration.

### Nouveaux manuscrits de travail

```text
1 _Matrice/article_01_comment_le_texte_arrive.md
2_Traitement/article_02_un_modele_continue.md
3_Qui parle/article_03_qui_parle_version_serie.md
4_Alignement/article_04_aligne_avec_qui.md
```

### États de document

Employer un front matter commun. Il **reprend les champs déjà utilisés** par la partie 3
publiée (`type`, `slug`, `status`, `title`, `description`, `image`, `image_alt`) et n’ajoute
que les champs de série et de suivi. Retirer les champs existants ferait échouer la
publication si la chaîne les consomme.

```yaml
---
type: note
slug: ...
status: draft
title: "..."
description: "..."
image: ...
image_alt: "..."
series: "Une phrase dans la machine"
part: 1
technical_review: pending
editorial_review: pending
sources_checked: 2026-08-04
---
```

Le champ `sources_checked` porte la date de la dernière vérification des sources primaires.
Il compte particulièrement pour la partie 3, adossée à un billet de recherche daté du
23 février 2026 dont l’interprétation peut être précisée ou contestée avant publication.

Valeurs de `status` recommandées :

1. `draft`
2. `structural-review`
3. `technical-review`
4. `copy-edit`
5. `ready`
6. `published`

---

## 14. Calendrier en douze séances

Les durées sont indicatives. L’ordre et les dépendances sont plus importants que les dates.

| Séance | Durée | Travail | Livrable |
|---|---:|---|---|
| 1 | 45 min | Valider promesse, public, titres et phrase témoin | Architecture verrouillée |
| 2 | 1 h | Construire le squelette propre de la partie 2 | Plan détaillé P2 |
| 3 | 2 h 30 | Monter la partie 2 à partir des deux sources | Version structurelle P2 |
| 4 | 1 h | Écrire le squelette et la scène d’ouverture de la partie 4 | Plan détaillé P4 |
| 5 | 2 h 30 | Rédiger la partie 4 depuis la page blanche | Version structurelle P4 |
| 6 | 2 h | Raccourcir et réordonner la partie 1 | Version structurelle P1 |
| 7 | 1 h 30 | Nuancer et raccourcir la partie 3 | Version série P3 |
| 8 | 2 h | Vérification technique des parties 1 et 2 | Corrections documentées |
| 9 | 2 h | Vérification documentaire des parties 3 et 4 | Sources vérifiées et datées |
| 10 | 2 h | Réviser le schéma des couches, créer celui de la partie 4, harmoniser les visuels | Quatre visuels cohérents |
| 11 | 1 h 30 | Harmoniser transitions, vocabulaire, chapeaux et conclusions | Série continue |
| 12 | 2 h | Relecture à voix haute, bêta-lecture et dernière coupe | Quatre articles prêts |

**Charge totale indicative : 21 à 24 heures.**

Trois écarts par rapport au calendrier initial en dix séances :

1. **La vérification passe de une à deux séances.** La partie 4 mobilise à elle seule huit
   références institutionnelles. Six des huit liens de `definition explication.md` portent le
   paramètre `?utm_source=chatgpt.com` : ils ont été collectés par l’intermédiaire d’un
   assistant et n’ont pas nécessairement été ouverts. La note comporte en outre quatre
   appels de note orphelins vers le rapport PDF, dont la référence n’a pas survécu à la
   copie. Deux heures ne suffisent pas pour les quatre articles.
2. **Une séance de travail graphique est ajoutée.** Le §12 demande de réviser
   `figure-vecteurs-couches.svg` et de créer un schéma pour la partie 4 ; aucune séance ne
   portait ce travail.
3. **La partie 2 passe avant la partie 1.** C’est le nœud structurel, et son montage libère
   la décision sur le triptyque, dont dépend la partie 4.

---

## 15. Tests de cohérence avant publication

### Test du lecteur pressé

Lire seulement :

- les quatre titres ;
- les quatre premiers paragraphes ;
- les trois transitions ;
- les quatre conclusions.

Le trajet complet doit rester compréhensible sans lire les développements.

### Test de la phrase témoin

Chercher « sucre », « nos ancêtres » et « nous » dans les quatre textes. Chaque occurrence doit accomplir une fonction nouvelle, et non répéter l’épisode précédent.

Le test se lit dans les deux sens. Une occurrence de trop est un défaut, mais **une
occurrence absente n’en est pas un** si l’exemple propre de l’article était plus
démonstratif (§3). La phrase témoin relie, elle ne démontre pas.

### Test du gabarit

Pour chaque article, retrouver dans le manuscrit les neuf temps du §10 et vérifier qu’ils
tombent dans les sections annoncées par la colonne **Gabarit** de son architecture cible. Un
temps introuvable signale soit une section à compléter, soit un temps à réattribuer
explicitement — jamais un oubli tacite.

### Test du niveau de preuve

Surligner avec quatre couleurs :

- faits et mécanismes établis ;
- simplifications pédagogiques ;
- hypothèses interprétatives ;
- questions philosophiques ou normatives.

Aucun passage ne doit changer de catégorie sans le signaler au lecteur.

### Test de l’anthropomorphisme

Pour chaque occurrence de « le modèle comprend », « sait », « veut », « choisit » ou « décide », vérifier si :

- le terme décrit précisément une opération ;
- il est annoncé comme une commodité de langage ;
- ou il doit être remplacé.

### Test de la voix

Passe distincte de celle du niveau de preuve : l’une vérifie ce que le texte affirme,
l’autre comment il le dit. Ne pas les mener ensemble.

La checklist du §19 du guide compte quinze items, dont sept sont déjà couverts ailleurs dans
cette feuille de route — commencer par un problème, distinction structurante, termes définis,
anthropomorphisme, vérification des sources, prise de position, question finale ouverte. Les
huit qui restent constituent le test.

- [ ] La contradiction est réellement examinée, non seulement mentionnée.
- [ ] Chaque référence ou exemple accomplit une fonction précise ; à défaut, il est supprimé.
- [ ] Le lecteur est associé au raisonnement par « nous » ou par « vous ».
- [ ] Le savoir revient à une expérience humaine.
- [ ] L’erreur n’est ni glorifiée ni effacée.
- [ ] Le texte alterne développement et phrases de tranchage.
- [ ] L’humour reste bref et utile : une pointe par article au maximum.
- [ ] Aucun paragraphe ne porte plus de trois noms propres.

Le dernier item vise la partie 4, dont la note source accumule huit références
institutionnelles en autant de paragraphes.

### Test des connecteurs

Compter, dans chaque manuscrit fini, les occurrences de « Très bien. Mais », « Il faut
distinguer », « On pourrait objecter », « Prenons un exemple », « Regardons précisément » et
« Voilà ». Aucune ne doit dépasser 1. Vérifier ensuite que le connecteur de pivot correspond
à celui que le §10 bis attribue à cette partie, et qu’aucun article ne reprend le dispositif
d’ouverture du précédent.

Chercher enfin « lundi matin » dans les quatre textes : une seule occurrence, en partie 4.

### Test d’autonomie

Chaque article doit pouvoir être lu seul, mais son dernier paragraphe doit donner envie de lire le suivant.

---

## 16. Checklist maîtresse

### Architecture

- [ ] Une promesse unique relie les quatre parties.
- [ ] Chaque article répond à une question différente.
- [ ] La progression mécanisme → génération → voix → alignement est explicite.
- [ ] La phrase témoin passe réellement d’un article à l’autre, sans être forcée.
- [ ] Les neuf temps du gabarit sont attribués section par section dans les quatre architectures.

### Manuscrits

- [ ] Partie 1 raccourcie et recentrée sur l’entrée.
- [ ] Partie 2 reconstruite en un seul texte.
- [ ] Partie 3 clairement présentée comme une note sur une hypothèse interprétative.
- [ ] Partie 4 réécrite comme article et non comme note de rapport.

### Exactitude

- [ ] Termes techniques définis au premier emploi.
- [ ] Architecture particulière et principe général ne sont pas confondus.
- [ ] Exemples fictifs signalés comme tels.
- [ ] Références primaires vérifiées.
- [ ] Incertitudes et limites explicites.

### Style

- [ ] Une contradiction principale par article.
- [ ] Une métaphore dominante par section.
- [ ] Les répétitions rhétoriques ont une fonction.
- [ ] Les conclusions tranchent sur ce que l’on peut affirmer.
- [ ] Chaque fin laisse ouverte la vraie question suivante.
- [ ] Le registre §16.2 est tenu : termes expliqués au premier emploi, un seul paradoxe par article, conclusion en critère.
- [ ] Les huit curseurs du §10 bis correspondent à ce que le texte fait réellement.
- [ ] Aucun connecteur signature n’apparaît deux fois dans le même article.
- [ ] « Lundi matin » n’apparaît qu’une fois dans toute la série.
- [ ] Aucun registre managérial ni cliché anti-IA.

### Publication

- [ ] Front matter harmonisé.
- [ ] Visuels cohérents et légendés.
- [ ] Liens et références testés.
- [ ] Relecture à voix haute effectuée.
- [ ] Une personne non spécialiste a compris les quatre transitions.
- [ ] Une personne compétente techniquement a relu les parties 1 et 2.
- [ ] Les quatre articles sont prêts avant la publication du premier, ou leurs architectures sont au minimum verrouillées.

---

## 17. Prochaine action concrète

Le manuscrit propre de la partie 2 est créé :

`2_Traitement/article_02_un_modele_continue.md`

Il contient uniquement :

1. le front matter du §13 ;
2. le titre et le chapeau de série ;
3. l’ouverture « Vous écrivez une phrase… » ;
4. les sept intertitres de l’architecture cible, avec leur budget de mots et les matériaux
   sources repérés par fichier et par ligne ;
5. le schéma existant ;
6. l’emplacement de l’encadré récapitulatif ;
7. la transition officielle vers la partie 3.

Ne rédiger les raccords qu’après ce montage. Cette opération permet de voir immédiatement les répétitions, les manques et les matériaux réellement utiles dans les deux brouillons actuels.

**Action suivante :** séance 3 du calendrier — remplacer, section par section, les blocs de
matériaux repérés par du texte rédigé, en commençant par la section 3, qui est la seule
dont le contenu n’existe qu’à l’état de notes techniques.
