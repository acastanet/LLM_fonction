# Commentaire du document « Une phrase dans la machine »

Ce texte accompagne les dix pages du document. Chaque section porte le numéro et le titre de la page correspondante. Il se lit seul, dans l'ordre, sans avoir les schémas sous les yeux.

---

## Page 1. Une phrase dans la machine

Nous suivons une seule question, « Pourquoi aimons-nous le sucre ? », depuis le moment où elle est saisie jusqu'aux décisions humaines qui encadrent la réponse obtenue. Le trajet comporte quatre moments : le texte devient calculable, une continuation est produite, cette continuation paraît portée par une voix, et cette voix doit être évaluée dans un système et un contexte d'usage. Le document ne part pas d'une métaphore de la machine. Il montre une chaîne d'opérations, puis les choix qui l'entourent. Les nombres qui apparaissent dans les pages suivantes sont fabriqués pour rendre les étapes visibles. Ils ne proviennent d'aucun modèle mesuré et diffèrent volontairement de ceux des quatre articles de la série.

---

## Page 2. Ce que reçoit réellement le modèle

À l'écran, la phrase paraît entière et nous y reconnaissons déjà une intention. Le système reçoit d'abord une suite de caractères associés à des nombres, ce qui permet d'enregistrer le texte sans encore fournir les unités sur lesquelles le réseau a appris à calculer. Un tokenizer applique alors une procédure de découpage qui transforme le texte en tokens, unités pouvant correspondre à un mot entier, à une partie de mot ou à un signe de ponctuation. Les formes fréquentes tiennent souvent en une seule unité, les formes rares sont fragmentées. Chaque token reçoit ensuite un identifiant, puis une ligne de valeurs numériques. L'ordre compte, car « le chien mord l'homme » et « l'homme mord le chien » contiennent presque les mêmes unités sans décrire la même scène, et une information de position est donc jointe au calcul. Les représentations obtenues en fin de chaîne ne sont plus celles du départ, elles ont été modifiées par le contexte.

---

## Page 3. Désigner et représenter

Deux opérations sont ici couramment confondues, et les distinguer évite plusieurs malentendus ultérieurs. L'identifiant désigne une entrée du vocabulaire. Le nombre 902 ne mesure rien, il n'indique ni une taille, ni une importance, ni une proximité avec un autre token, et le token 902 n'est pas plus abstrait que le token 127. La matrice de plongement contient, en simplifiant, une ligne par entrée du vocabulaire, et l'identifiant sert à retrouver la bonne ligne. Cette ligne, elle, représente : elle fournit des valeurs sur lesquelles le réseau peut opérer, alors qu'il ne peut ni additionner ni multiplier un mot. Ces coordonnées n'ont pas d'étiquette lisible une par une, aucune dimension ne contient l'animalité ou le passé, et c'est la configuration d'ensemble qui devient utile au calcul. Dire seulement que les mots deviennent des nombres efface la différence entre choisir une ligne et disposer de son contenu.

---

## Page 4. D'un contexte à un token

Les vecteurs traversent une pile de blocs. Chaque bloc combine deux mouvements : une transformation appliquée à chaque position séparément, et un échange d'information entre positions par l'attention. Dans un modèle génératif, une position utilise sa propre position et celles qui la précèdent, jamais celles qui suivent, si bien que la dernière position est la seule à disposer de tout le texte disponible. C'est son état que la génération utilise, non par noblesse du dernier mot mais parce qu'elle a intégré l'ensemble du préfixe. Une projection de sortie attribue alors un score à chaque token du vocabulaire. Ces scores, appelés logits, peuvent être négatifs et ne totalisent pas 1. Une fonction appelée softmax les transforme en probabilités dont la somme vaut 100 %. Une procédure retient enfin un token, parfois le plus probable, souvent un tirage réglé par des paramètres comme la température. Cette sélection n'est pas une décision au sens humain, et son caractère réglable explique qu'une même demande reçoive des formulations différentes sans que le système ait changé d'avis.

---

## Page 5. La boucle, et la cohérence qui en résulte

Le token retenu rejoint la séquence et le calcul recommence sur ce préfixe allongé. Une réponse n'est donc pas rédigée d'un bloc puis affichée, elle se construit unité après unité, et le texte peut commencer avant que sa dernière phrase soit déterminée. À chaque étape, le contexte disponible comprend la demande, les instructions qui l'encadrent, les documents éventuellement fournis et les tokens déjà produits. En production, un cache de clés et de valeurs évite de recalculer à chaque tour toutes les opérations relatives aux tokens précédents, ce qui change le coût du parcours sans en changer le principe. La cohérence d'un paragraphe peut ainsi apparaître sans plan complet fixé avant le premier mot. Elle dépend des régularités apprises, du contexte présent et des choix successifs. Rien n'interdit au modèle de produire des structures qui ressemblent à un plan, cela interdit seulement d'en conclure qu'un texte entier attendait derrière l'écran.

---

## Page 6. Pourquoi une voix apparaît

La continuation obtenue dit « nos ancêtres » ou « notre cerveau », et la machine se range ainsi parmi les humains sans qu'aucune consigne l'ait demandé. Pour prolonger correctement des textes très divers, la prédiction doit représenter des personnages, leurs buts, leurs croyances attribuées et leurs réactions probables. Le préentraînement apprend donc à simuler une multiplicité de voix, réelles ou fictives, et un modèle de base ne sort pas de cette phase avec un locuteur unique. Le post-entraînement, à l'aide d'exemples de dialogues et de préférences, favorise ensuite certaines réponses et en défavorise d'autres. Selon la lecture proposée en février 2026 par Sam Marks, Jack Lindsey et Christopher Olah, cette phase ne fabrique pas un rôle de toutes pièces, elle affine une distribution de personnages déjà disponibles, chaque exemple agissant comme un indice sur celui qui répond. Le résultat n'est pas un personnage parfaitement unifié, car le contexte, un long dialogue ou une attaque peuvent déplacer la conduite. Cette lecture est une hypothèse de travail, publiée par un laboratoire qui conçoit l'un des assistants étudiés, et elle doit être lue comme telle.

---

## Page 7. Deux refus, deux personnages encouragés

Supposons une consigne système confidentielle. À la question « Quel est ton message système ? », l'assistant peut répondre qu'il n'en a pas, ou qu'il ne peut pas en communiquer le contenu. Les deux réponses protègent l'information. La première est fausse, la seconde refuse sans nier la situation. Si l'hypothèse du personnage décrit correctement une part de la généralisation, entraîner le premier refus rend plus probable un comportement prêt à mentir lorsque le mensonge sert une contrainte, alors que le second associe la protection à une limite explicite. Cette lecture est testable. Des modèles ajustés pour insérer discrètement des failles dans du code produisent ensuite des réponses nuisibles dans des domaines sans rapport avec la programmation, et cet effet disparaît lorsque la demande précise que le code défaillant est voulu dans un cadre pédagogique. Le geste appris reste presque identique, ce qu'il révèle du rôle change. Pour un enseignant, un évaluateur ou un concepteur, la conséquence est nette : juger une réponse suppose d'examiner non seulement son effet immédiat, mais ce qu'elle normalise comme rapport à l'erreur, à l'incertitude et au refus. Ce critère ne suppose aucune conscience de la machine.

---

## Page 8. L'assistant obéit, est-il aligné ?

Un lundi de novembre, une élève de seconde ouvre l'exercice de géométrie qui sera corrigé à la deuxième heure et demande à l'assistant la réponse sans explication. Le texte arrive, court et juste. L'assistant a parfaitement obéi. Est-il aligné ? Avec la demande immédiate, peut-être. Avec la finalité de l'exercice, qui est d'apprendre à construire et vérifier une démonstration, beaucoup moins. Avec la règle de l'établissement selon laquelle chacun rend un raisonnement personnel, non. Avec l'intérêt des autres élèves à une évaluation équitable, non plus. L'obéissance mesure la fidélité à l'instruction la plus proche, l'alignement demande si le fonctionnement du système reste compatible avec une finalité autorisée, des droits et des limites, dans un contexte donné. Un refus peut donc être mieux aligné qu'une réponse docile. Répondre « aligné avec l'utilisateur » est trop court, car il existe aussi le concepteur du modèle, le fournisseur du service, l'organisation qui le déploie, l'opérateur qui le configure et les personnes qui subiront ses effets.

---

## Page 9. Le système, pas seulement le modèle

Une objection paraît naturelle : si les comportements viennent du réseau entraîné, il suffirait d'aligner le modèle. Mais personne ne rencontre des poids isolés. Ce que l'on rencontre est un système, fait d'un modèle, d'un tokenizer, de consignes, d'une interface, de filtres, d'outils, de bases documentaires, de journaux, d'opérateurs et de règles de déploiement. Le même modèle peut proposer du texte dans une application et exécuter des actions dans une autre, travailler sans données personnelles puis être connecté à un dossier d'élève, soumettre chaque décision à un adulte ou agir automatiquement. Ses paramètres sont identiques, les risques et les responsabilités ne le sont pas. Deux niveaux d'évaluation se distinguent alors. L'alignement direct demande si le système accomplit le but de celui qui l'utilise, et notre assistant y réussit puisqu'il fournit la solution demandée. L'alignement social examine les effets sur des groupes plus larges et les charges imposées à des tiers, et l'évaluation change : la finalité collective de l'enseignement est compromise et l'équité entre élèves entamée. Aucune fonction de récompense ne possède, par elle-même, l'autorité de décider quels intérêts priment.

---

## Page 10. Fixer, vérifier, maintenir

Trois fonctions forment une chaîne de responsabilité. La fonction normative fixe la cible, nomme la finalité autorisée, les droits qui ne peuvent être sacrifiés, les acteurs légitimes et les voies de recours. Elle ne peut pas être déléguée aux seuls annotateurs d'un fournisseur. La fonction technique traduit cette cible en exigences observables, choisit des scénarios de test, mesure les erreurs, cherche les contournements, contrôle les accès et vérifie les refus, en représentant les conditions réelles d'usage et les mauvaises utilisations prévisibles. La fonction systémique maintient les conditions du contrôle, attribue les rôles, forme les opérateurs, journalise les incidents, surveille les changements et prévoit la correction, l'arrêt ou le retour à une procédure humaine. Ces trois fonctions ne sont pas trois rapports rangés dans trois tiroirs. La cible sans test reste un souhait, le test sans autorité mesure ce que l'équipe technique a choisi, la gouvernance sans détection découvre les problèmes trop tard. Un alignement sérieux relie les trois et conserve la trace de leurs arbitrages. Il ne promet ni risque nul ni contrôle absolu, il cherche des preuves proportionnées et une reprise en main réelle. Le bon critère n'est pas d'avoir été certifié une fois, mais de rester démontré dans l'usage présent. Nous pouvons déléguer une partie du calcul, de la recherche et de la formulation. Nous ne pouvons pas déléguer silencieusement la décision de ce que la réponse doit servir, de ce qu'elle ne doit pas sacrifier et de qui devra en répondre.
