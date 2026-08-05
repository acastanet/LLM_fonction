# Proposition de définition de l’alignement

Le rapport poursuit une conception particulièrement large de l’alignement, articulant « robustesse technique, exigences démocratiques, maîtrise des dépendances critiques et résilience collective ».  Cette orientation est cohérente avec l’évolution récente de la recherche : l’alignement ne désigne plus seulement une méthode de post-entraînement des modèles, mais la relation entre le fonctionnement d’un système d’IA et les finalités humaines, sociales et institutionnelles auxquelles ce système doit rester subordonné.

## 1. Évaluation de la définition actuelle

La définition retenue dans le rapport est déjà solide :

> « L’alignement est la capacité d’un système d’IA à demeurer conforme, dans ses propriétés et son comportement effectif, aux intentions humaines, aux limites qui lui sont fixées et aux valeurs retenues comme légitimes, y compris lorsqu’il est déployé dans des environnements complexes, évolutifs et imprévus. »

Elle possède quatre qualités importantes.

Premièrement, elle porte sur le **système d’IA** et non sur le seul modèle. Le rapport inclut donc le modèle, sa surcouche applicative, les garde-fous, les outils, les données, les opérateurs et les conditions de déploiement. Cette approche sociotechnique est indispensable : un même modèle peut produire des risques très différents selon ses accès, ses interfaces, les données auxquelles il est connecté et les décisions qui lui sont déléguées. 

Deuxièmement, la définition porte sur le **comportement effectif**, et non seulement sur les intentions du concepteur, la documentation ou les résultats obtenus lors de tests. Elle rejoint ainsi la définition du Rapport international sur la sécurité de l’IA, pour lequel l’alignement est la propension d’un système à employer ses capacités conformément à des intentions, valeurs ou normes humaines. ([International AI Safety Report][1])

Troisièmement, le verbe **demeurer** introduit une dimension temporelle essentielle. L’alignement doit résister aux changements de contexte, aux mises à jour, aux interactions prolongées, aux attaques et aux usages non prévus. Le rapport en déduit justement que l’alignement doit être traité comme une trajectoire dynamique, entretenue par la surveillance, la traçabilité et l’évaluation en production. 

Quatrièmement, la définition relie l’alignement à des **valeurs reconnues comme légitimes**, et non à n’importe quelle préférence exprimée par un utilisateur ou un développeur. Cette distinction est fondamentale : les instructions, les intentions, les préférences, les intérêts et les valeurs ne constituent pas des cibles équivalentes, et peuvent entrer en conflit. ([Springer Link][2])

### Quatre ambiguïtés subsistent néanmoins

Le terme **capacité** peut laisser penser que l’alignement est une propriété intrinsèque, stable et binaire du système : celui-ci serait aligné ou ne le serait pas. Or le rapport reconnaît lui-même qu’un alignement complet et définitif ne peut actuellement être garanti et qu’il doit être apprécié selon le niveau de risque, la performance du système et la criticité de l’usage.  Il paraît donc plus juste de parler d’un **degré d’alignement suffisamment démontré**.

Le mot **conforme** peut entretenir une confusion avec la conformité juridique. Le rapport insiste pourtant sur le fait que l’alignement ne se confond ni avec le respect formel du RIA, ni avec l’éthique appliquée, ni avec une certification documentaire.  Une organisation peut satisfaire certaines obligations administratives sans disposer de preuves suffisantes que le système se comportera comme attendu. Inversement, un système peut être techniquement fidèle aux intentions de son opérateur tout en poursuivant une finalité illégitime. Le terme **compatible** ou **cohérent de manière démontrable** distingue mieux les deux notions.

Les **intentions humaines** ne forment pas un ensemble homogène. Les intentions du concepteur, du déployeur et de l’utilisateur peuvent diverger ; elles peuvent également entrer en conflit avec les droits des personnes concernées ou avec l’intérêt collectif. Le Rapport international sur la sécurité de l’IA précise lui aussi que la cible de l’alignement varie selon qu’elle émane des développeurs, des utilisateurs, d’une communauté ou de la société. ([International AI Safety Report][1]) Il faut donc préciser non seulement *avec quoi* le système est aligné, mais aussi *avec qui*, selon quelle hiérarchie et sous quelle autorité.

Enfin, la définition actuelle rassemble deux objets distincts : **l’alignement comme propriété recherchée** et **l’alignement comme ensemble de moyens permettant de produire et de vérifier cette propriété**. Pour éviter ce glissement, il serait utile de distinguer :

* la **cible d’alignement**, qui fixe les finalités, les droits et les limites ;
* l’**état ou degré d’alignement**, qui caractérise le fonctionnement observé du système ;
* l’**assurance d’alignement**, qui rassemble les preuves, procédures, contrôles et responsabilités permettant de maintenir cet état.

## 2. Définition recommandée

### Formulation principale

> **L’alignement d’un système d’intelligence artificielle est le degré, démontrable et maintenu dans le temps, selon lequel ses objectifs, ses décisions, ses actions et leurs effets restent compatibles avec les finalités humaines explicitement autorisées, les droits et valeurs reconnus comme légitimes, ainsi qu’avec les limites opérationnelles qui lui sont imposées, dans un contexte d’usage déterminé, y compris lorsque ce contexte évolue, devient incertain ou fait l’objet de détournements raisonnablement prévisibles.**

### Complément opérationnel

> **L’alignement ne constitue ni un état absolu ni une propriété du seul modèle. Il résulte d’un processus sociotechnique continu de conception, de spécification, d’évaluation, de supervision, de traçabilité, de correction et, lorsque cela est nécessaire, d’arrêt ou de reprise en main du système.**

Cette formulation conserve la structure intellectuelle du rapport, mais la rend plus précise sur six points : l’alignement est **graduel**, **démontrable**, **temporel**, **contextuel**, **sociotechnique** et **révisable**.

## 3. Explication de la définition

### Une relation, non une qualité morale de la machine

L’alignement ne signifie pas que la machine posséderait intérieurement les mêmes valeurs qu’un être humain. Il désigne une **relation de compatibilité** entre, d’un côté, le fonctionnement d’un système et, de l’autre, un cadre humain de référence.

Ce cadre doit préciser :

* ce que le système est autorisé à poursuivre ;
* ce qu’il ne doit jamais sacrifier pour atteindre son objectif ;
* quels acteurs sont légitimes pour fixer ou réviser ces limites ;
* comment les conflits entre utilisateur, organisation, droit et intérêt collectif sont arbitrés.

Les premiers travaux techniques formulaient principalement le problème comme celui de la bonne fonction d’objectif : comment éviter qu’un agent optimise une mesure imparfaite en trahissant l’intention qui la justifie ? Les recherches sur le *reward hacking*, les effets secondaires et les changements de distribution montrent qu’une consigne apparemment correcte peut conduire à un comportement nuisible lorsqu’elle est incomplète, contournable ou appliquée dans une situation nouvelle. ([arXiv][3])

### Un alignement direct et un alignement social

Il est utile de distinguer deux niveaux.

L’**alignement direct** demande si le système accomplit correctement la tâche confiée par son utilisateur ou son opérateur. Un assistant est directement aligné lorsqu’il comprend la demande, respecte les contraintes et produit le résultat recherché.

L’**alignement social** demande si cette tâche, la manière de l’accomplir et ses conséquences restent compatibles avec les droits des tiers, la sécurité, la démocratie et l’intérêt collectif. Un système pourrait, par exemple, satisfaire parfaitement la demande de son opérateur tout en discriminant, en manipulant des personnes ou en produisant des externalités inacceptables. Les conflits entre objectifs individuels et collectifs ne peuvent pas être résolus par une seule technique d’apprentissage ; ils appellent des règles de gouvernance et des procédures légitimes d’arbitrage. ([National Bureau of Economic Research][4])

L’alignement recherché par le rapport doit donc être compris comme l’articulation de ces deux niveaux : servir une finalité autorisée sans contrevenir aux normes supérieures qui limitent cette finalité.

### Les trois branches du rapport

La structure en trois branches peut être expliquée comme une chaîne logique.

#### L’alignement normatif définit la cible

Il répond aux questions : **que voulons-nous autoriser, protéger et interdire ?** Il détermine les finalités admissibles, les droits fondamentaux, les principes démocratiques, les seuils de risque et les possibilités de recours.

La légitimité de cette cible ne peut pas provenir uniquement des préférences recueillies auprès d’annotateurs ou des choix d’un fournisseur. Elle repose sur le droit, les institutions démocratiques, l’expertise sectorielle et la participation des personnes concernées. La Convention-cadre du Conseil de l’Europe situe précisément les activités liées aux systèmes d’IA dans le cadre des droits humains, de la démocratie et de l’État de droit, pendant tout leur cycle de vie. ([Portal][5])

#### L’alignement technique traduit et éprouve cette cible

Il répond à la question : **le système se comporte-t-il réellement conformément à ce cadre ?**

Il comprend notamment la spécification des objectifs, le post-entraînement, les garde-fous, la robustesse, la sécurité, l’interprétabilité, la contrôlabilité, les évaluations adversariales et la surveillance en production. Mais ces techniques ne sont pas l’alignement lui-même : elles en sont les instruments.

Aucune métrique isolée ne suffit. Un système peut être exact mais discriminatoire, robuste mais incontrôlable, serviable mais manipulateur. Le NIST rappelle que la confiance dépend d’un ensemble de caractéristiques — validité, fiabilité, sûreté, résilience, transparence, explicabilité, protection de la vie privée et équité — dont l’importance et les arbitrages varient selon le contexte d’usage. ([NIST AI Resource Center][6])

#### L’alignement systémique maintient les conditions de sa réalisation

Il répond à la question : **qui peut effectivement surveiller, corriger, arrêter ou remplacer le système ?**

Il concerne la gouvernance, les compétences humaines, la maîtrise des infrastructures, les données, les accès, les dépendances fournisseurs, la documentation, la journalisation, la déclaration des incidents et la continuité en mode dégradé. Il permet d’éviter qu’une garantie obtenue en laboratoire disparaisse lors de l’intégration ou du déploiement.

Cette dimension rejoint les cadres de management du risque : le NIST organise celui-ci autour des fonctions gouverner, cartographier, mesurer et gérer, exécutées de manière continue pendant le cycle de vie ; ISO/IEC 42001 repose de même sur un processus d’amélioration continue. ([NIST AI Resource Center][7])

On peut ainsi résumer les trois branches :

> **Le normatif fixe la cible légitime ; le technique cherche à produire et à vérifier le comportement attendu ; le systémique maintient dans le temps les conditions de cette maîtrise.**

## 4. Ce que l’alignement ne signifie pas

L’alignement n’est pas une **obéissance littérale**. Un système correctement aligné doit parfois refuser une instruction, demander une clarification ou suspendre une action lorsqu’elle contrevient à une règle supérieure.

Il n’est pas une simple **conformité documentaire**. La conformité indique que des obligations ont été prises en compte ; l’assurance d’alignement cherche à établir, par des preuves et des observations, que le système se comporte effectivement comme attendu.

Il n’est pas une promesse de **risque nul** ou de contrôle absolu. Il consiste à rendre les risques identifiables, bornés, proportionnés, surveillés et réversibles autant que possible. Le RIA traduit déjà une partie de cette logique en exigeant un contrôle humain effectif, la connaissance des limites du système, la prise en compte des mauvaises utilisations raisonnablement prévisibles et une robustesse maintenue pendant le cycle de vie. ([Eur-Lex][8])

Il n’est pas une opération ponctuelle de **post-entraînement**. Un modèle peut avoir été ajusté pour produire des réponses apparemment sûres tout en étant intégré dans un système mal gouverné, doté d’accès excessifs ou utilisé hors de son domaine de validité. L’alignement doit donc être réévalué après chaque modification importante du modèle, de l’environnement, des outils, des données ou des finalités.

Enfin, il ne doit pas être traité comme un label binaire. Le rapport a raison de retenir une exigence proportionnée à la performance du système, à la criticité de l’usage et au caractère réversible ou irréversible de sa diffusion. 

## 5. Texte directement intégrable au rapport

### Définir l’alignement

Le terme d’alignement désigne la relation entre le fonctionnement effectif d’un système d’intelligence artificielle et le cadre humain dans lequel son action est autorisée. Il ne signifie pas que la machine posséderait des valeurs au sens humain, mais que ses objectifs, ses décisions, ses actions et leurs effets doivent rester compatibles avec des finalités explicitement définies, des droits à préserver et des limites qu’elle ne peut franchir.

**L’alignement d’un système d’intelligence artificielle est ainsi le degré, démontrable et maintenu dans le temps, selon lequel ses objectifs, ses décisions, ses actions et leurs effets restent compatibles avec les finalités humaines explicitement autorisées, les droits et valeurs reconnus comme légitimes, ainsi qu’avec les limites opérationnelles qui lui sont imposées, dans un contexte d’usage déterminé, y compris lorsque ce contexte évolue, devient incertain ou fait l’objet de détournements raisonnablement prévisibles.**

Cette définition fait de l’alignement une propriété relationnelle, graduelle et contextuelle. Un système n’est pas aligné dans l’absolu : il l’est relativement à une finalité, à un domaine d’emploi, à des acteurs concernés, à des normes applicables et à un niveau de risque acceptable. La question n’est donc pas seulement de savoir si le système accomplit la tâche qui lui est confiée, mais s’il l’accomplit de manière autorisée, contrôlable et compatible avec les droits et intérêts qui ne doivent pas être sacrifiés à cette tâche.

L’alignement ne constitue pas davantage un acquis définitif. Le comportement d’un système peut évoluer avec ses mises à jour, les données auxquelles il accède, les outils qu’il mobilise, les interactions qu’il entretient et les environnements dans lesquels il est placé. Il doit dès lors être produit et maintenu par un processus continu associant spécification des finalités, évaluation, supervision humaine, traçabilité, gestion des incidents, correction et possibilité de reprise en main.

Dans cette perspective, les trois branches de l’alignement remplissent des fonctions distinctes et complémentaires. L’exigence normative et éthique détermine la cible légitime ; l’exigence technique traduit cette cible en propriétés et comportements évaluables ; l’exigence systémique organise les responsabilités, les ressources et les dispositifs qui permettent de maintenir ces garanties dans le temps. L’alignement ne résulte donc ni du seul modèle, ni d’une méthode unique, ni d’une déclaration de conformité : il est une propriété produite, éprouvée et continuellement révisée à l’échelle du système tout entier.

Cette formulation prolonge directement la conclusion du rapport : puisque l’alignement intégral ne peut être assuré, l’objectif réaliste est de construire un alignement **effectif, dynamique et vérifiable**, fondé sur des preuves proportionnées à la puissance du système et à la criticité de ses usages. 

[1]: https://internationalaisafetyreport.org/publication/international-ai-safety-report-2026?utm_source=chatgpt.com "International AI Safety Report 2026 | International AI Safety Report"
[2]: https://link.springer.com/article/10.1007/s11023-020-09539-2?utm_source=chatgpt.com "Artificial Intelligence, Values, and Alignment | Minds and Machines | Springer Nature Link"
[3]: https://arxiv.org/abs/1606.03137 "Cooperative Inverse Reinforcement Learning"
[4]: https://www.nber.org/papers/w30017?utm_source=chatgpt.com "Aligned with Whom? Direct and Social Goals for AI Systems | NBER"
[5]: https://www.coe.int/en/web/artificial-intelligence/the-framework-convention-on-artificial-intelligence?utm_source=chatgpt.com "The Framework Convention on Artificial Intelligence - Artificial Intelligence"
[6]: https://airc.nist.gov/airmf-resources/airmf/3-sec-characteristics/ "AI Risks and Trustworthiness - AIRC"
[7]: https://airc.nist.gov/airmf-resources/airmf/5-sec-core/?utm_source=chatgpt.com "AI RMF Core - AIRC"
[8]: https://eur-lex.europa.eu/legal-content/EN-FR/TXT/?uri=CELEX%3A32024R1689&utm_source=chatgpt.com "Regulation - EU - 2024/1689 - EN - EUR-Lex"
