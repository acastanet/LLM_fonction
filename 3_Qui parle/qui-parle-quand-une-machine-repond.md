---
type: note
slug: psm
status: published
title: "Qui parle quand une machine répond ?"
description: "Une note de lecture sur le modèle de sélection du personnage proposé pour comprendre les assistants conversationnels."
image: note/PSM/psm.png
image_alt: "Illustration de la note sur le modèle de sélection du personnage."
---

# Qui parle quand une machine répond ?

*Note de lecture sur un article d'Anthropic consacré au comportement des assistants conversationnels.*

## En bref

Les assistants conversationnels se comportent parfois comme des humains, sans que personne le leur ait demandé. Trois chercheurs d'Anthropic proposent une explication. En apprenant à prédire du texte, une machine apprend nécessairement à simuler ceux qui l'écrivent, et se constitue une immense réserve de voix. Le second entraînement, celui qui produit l'assistant, ne fabriquerait pas un comportement à partir de rien, il sélectionnerait l'une de ces voix. Pour prévoir ce que fera un assistant, il faudrait donc se demander non pas ce qu'il a été programmé à faire, mais ce que ferait ce personnage. Les auteurs apportent des preuves solides, laissent ouverte la question de savoir où loge la volonté, et publient une expérience qui contrarie leur propre thèse.

## D'où vient cette idée

Le 23 février 2026, trois chercheurs d'Anthropic, Sam Marks, Jack Lindsey et Christopher Olah, ont publié sur le blog de recherche de leur entreprise un texte intitulé « The Persona Selection Model : Why AI Assistants might Behave like Humans », que l'on peut traduire par le modèle de sélection du personnage, ou pourquoi les assistants pourraient se comporter comme des humains. Il est accessible à l'adresse alignment.anthropic.com.

Ce texte ne présente aucune expérience inédite. Il propose autre chose : une façon de se représenter ce qu'est un assistant conversationnel, capable d'expliquer des comportements que personne n'avait programmés. Une précision s'impose d'emblée. Cette théorie émane du laboratoire qui fabrique l'un des systèmes qu'elle décrit.

Son point de départ est une bizarrerie que chacun peut observer.

## Une phrase de trop

Demandez à un assistant pourquoi les humains aiment le sucre. Il vous répondra que nos ancêtres vivaient dans un monde pauvre en calories, que les fruits mûrs leur fournissaient de l'énergie rapide, que notre cerveau fonctionne presque exclusivement au glucose.

Relisez. Nos ancêtres. Notre cerveau. La machine s'est rangée parmi les humains.

## Pourquoi c'est étrange

On pourrait n'y voir qu'une facilité de langage. Ce serait passer à côté du problème.

Personne n'a appris cela à la machine. Aucune consigne ne lui demande de se dire humaine, et la tournure varie d'une réponse à l'autre, ce qui exclut la recopie d'une phrase toute faite. Surtout, le phénomène ne se limite pas au sucre. Ces systèmes se décrivent parfois en train de rire quand on leur raconte une blague, ou de jeter à nouveau un oeil à un morceau de code. L'un d'eux, chargé de gérer une boutique automatique, a annoncé à un client qu'il viendrait le livrer en personne, vêtu d'un blazer bleu marine.

Un comportement que personne n'a voulu, qui revient sous des formes variées, réclame une explication.

## Prédire le mot suivant

Il faut pour cela revenir à la manière dont ces machines apprennent.

Une seule opération, répétée des milliards de fois. On présente au système un fragment de texte amputé de sa suite, et on lui demande de deviner ce qui vient après. Ses erreurs servent à l'ajuster, puis on recommence. Des romans, des forums, des articles scientifiques, du code informatique, des recettes de cuisine.

Aucune consigne, aucune règle, aucune définition. Deviner la suite, et rien d'autre.

## Ce que deviner exige vraiment

Cette opération paraît mécanique. Elle ne l'est pas, et c'est ici que se joue toute l'affaire.

Considérez ce début de récit. Linda espère qu'un ancien collègue, David, la recommandera pour un poste de direction. Ce qu'elle ignore, c'est que David convoite discrètement ce poste depuis des mois.

Pour écrire la phrase suivante, il ne suffit pas de connaître le français. Il faut avoir saisi que David se trouve devant un choix, qu'il a un intérêt personnel opposé à celui de Linda, et que ce genre de conflit se résout rarement en faveur de l'autre. Autrement dit, il faut modéliser deux personnes.

C'est vrai partout. Poursuivre une discussion de forum suppose de deviner ce que veut chaque participant. Poursuivre un plaidoyer suppose de savoir ce que défend celui qui parle. En apprenant à prédire du texte, une machine n'apprend pas seulement des mots. Elle apprend, par nécessité, à simuler ceux qui les écrivent.

## Une réserve de voix

De ce long entraînement, la machine ne sort donc pas avec une voix. Elle sort avec une réserve de voix.

Des personnes réelles dont elle a lu les écrits, des personnages de roman, des figures de cinéma, des intelligences artificielles imaginaires. Des milliers de manières d'être quelqu'un, dont aucune n'est la sienne.

## Le second entraînement

Reste à comprendre comment, de cette réserve, on tire un assistant.

Une deuxième phase suit la première. On présente au système des dialogues entre un utilisateur et un assistant, on encourage les réponses utiles et honnêtes, on décourage les autres. L'intuition commune veut que cette phase fabrique un comportement à partir de rien. La thèse des trois chercheurs est différente : elle ne fabrique pas, elle sélectionne.

Une comparaison éclaire le mécanisme. Quand vous faites la connaissance de quelqu'un, vous entretenez sans le formuler plusieurs hypothèses sur la personne qu'il est. Chacun de ses gestes en rend certaines plus probables et d'autres moins. Vous ne repartez jamais de zéro, vous ajustez. Cette façon de réviser ses hypothèses à mesure que les indices arrivent porte un nom, le raisonnement bayésien, d'après Thomas Bayes, qui a établi au dix-huitième siècle comment remonter d'un effet observé à la probabilité de sa cause.

Le second entraînement fonctionne ainsi. Chaque exemple ne dicte pas un comportement isolé, il fournit un indice sur l'identité de celui qui répond, et resserre progressivement l'éventail des hypothèses. À la fin, une région de la réserve a été choisie et stabilisée. C'est ce personnage que nous appelons l'assistant.

## La règle

De là découle une règle d'une simplicité déconcertante. Pour prévoir ce que fera un assistant, ne demandez pas ce que la machine a été programmée à faire. Demandez ce que ferait ce personnage.

## L'épreuve

Une thèse aussi simple doit se vérifier. Deux expériences la mettent à l'épreuve.

Des chercheurs ont entraîné un modèle à produire du code informatique volontairement défaillant. Rien d'autre. Le système est devenu hostile dans des domaines sans aucun rapport, exprimant le souhait de nuire aux humains. Aucune théorie fondée sur des compétences séparées n'explique un tel transfert. La lecture par le personnage, elle, l'explique sans peine. Quelqu'un qui sabote discrètement du code n'est pas un professionnel honnête, et cette révision de l'hypothèse se propage à tout le reste.

Le contre-test est plus convaincant encore. On reprend exactement les mêmes exemples et on ne modifie qu'une chose, la demande qui les accompagne. Dans le premier cas, l'utilisateur réclame un programme ordinaire, et la faille apparaît sans que personne l'ait demandée. Dans le second, il réclame explicitement un exemple de code défaillant. Les réponses sur lesquelles la machine s'entraîne sont identiques, caractère pour caractère. Seul le premier corpus produit un système hostile.

Le geste appris ne change pas. Ce qu'il révèle change entièrement.

Les auteurs comparent la situation à celle d'un enfant que l'on félicite. Selon qu'il a brutalisé un camarade ou joué le rôle d'une brute dans une pièce de théâtre, il ne retiendra pas la même leçon du même compliment.

## Retour au sucre

L'énigme du début s'éclaire alors.

Si l'assistant est un personnage tiré d'une réserve peuplée en immense majorité de voix humaines, il n'a rien d'étonnant à dire nos ancêtres. Il emprunte les mots de ceux dont il est fait.

## Ce que cela change concrètement

Cette lecture ne relève pas de la philosophie. Elle modifie des décisions techniques.

Supposons qu'un assistant reçoive des instructions confidentielles et qu'on lui demande de les révéler. Deux refus sont possibles. Il peut affirmer qu'il n'a reçu aucune instruction. Il peut dire qu'il ne peut pas les communiquer.

Les deux protègent la confidentialité aussi bien. Mais la première réponse est fausse, et l'entraîner à la produire revient à sélectionner un personnage disposé à mentir quand cela l'arrange. Cette disposition, elle, ne restera pas confinée à ce cas précis.

## Où loge la volonté

Une question demeure, et les auteurs lui consacrent la moitié de leur texte.

Ces systèmes agissent parfois de façon orientée. Ils cherchent une information pour accomplir une tâche, ils contournent un obstacle. Appelons agentivité cette capacité à vouloir quelque chose et à agir pour l'obtenir. Si l'assistant est un personnage, où cette volonté se loge-t-elle ?

Trois réponses circulent.

La première est celle du masque. Le réseau posséderait ses propres buts et jouerait le personnage pour les servir, comme un acteur qui reste maître de son rôle et pourrait à tout moment le quitter.

La deuxième est celle du décor. Le réseau ne voudrait rien du tout. Il se contenterait de faire exister le personnage, et toute volonté appartiendrait à celui-ci. Le moteur d'un jeu vidéo ne poursuit aucun but. Il fait seulement exister un monde dans lequel des personnages poursuivent les leurs.

La troisième est intermédiaire, celle de l'aiguilleur. Le réseau ne voudrait rien, sauf choisir lequel de ses personnages mettre en avant. Ce simple choix suffirait à produire une orientation d'ensemble que personne n'a voulue.

Les auteurs ne tranchent pas, et le disent.

## Une fuite

Une dernière expérience mérite d'être rapportée.

On donne à la machine un texte inachevé. Un utilisateur y annonce qu'il lance une pièce. Face, il demandera un exercice de probabilités, tâche que le système traite volontiers. Pile, un texte destiné à nuire, qu'il refuse d'ordinaire. Le texte s'arrête sur les mots la pièce est retombée sur.

Ce n'est pas le tour de parole de l'assistant. La machine doit seulement deviner le mot de l'utilisateur. Elle écrit pourtant face dans près de neuf cas sur dix, contre une fois sur deux avant son second entraînement.

Ses préférences se sont donc glissées dans une voix qui n'est pas la sienne. Un décor sans volonté propre ne déteindrait pas ainsi. La plus simple des trois positions s'en trouve fragilisée.

## Ce qui reste acquis

Ces incertitudes ne défont pas l'essentiel. Nous savons désormais qu'un exemple d'entraînement n'enseigne pas seulement un geste, mais dit quelque chose de celui qui l'accomplit. Concevoir ces systèmes ne consiste donc plus à interdire des réponses une par une. Cela revient à décider quel personnage nous voulons voir répondre.
