# Grokking : quand un réseau généralise après avoir déjà mémorisé

***Un réseau de neurones donne toutes les bonnes réponses. Très bien. Mais qu’a-t-il appris ?***

La question paraît presque absurde. S’il répond juste, c’est bien qu’il sait. Pourtant, en apprentissage automatique, il faut distinguer deux choses très différentes : réussir les exemples rencontrés pendant l’entraînement et être capable de réussir sur de nouveaux exemples de la même tâche.

Au début des années 2020, Alethea Power et ses collègues chez OpenAI vont rencontrer cette distinction d’une manière particulièrement spectaculaire. Leur objectif est d’étudier la généralisation dans un cadre suffisamment simple pour pouvoir observer précisément ce qui se passe. Ils choisissent de petits problèmes mathématiques, notamment des opérations modulaires.[^1]

Imaginez une horloge. Sur une horloge de douze heures, 11 + 3 ne donne pas 14, mais 2. Dans leurs expériences, les chercheurs travaillent notamment avec des opérations modulo 97. Une partie des opérations est montrée au réseau pendant son entraînement. Les autres sont gardées de côté pour l’évaluer ensuite.[^1]

***Pourquoi cette séparation ?***

Parce qu’elle permet de poser deux questions différentes. Le réseau sait-il répondre aux exercices qu’il a rencontrés ? Et sait-il appliquer ce qu’il a appris à des opérations qu’il n’a jamais vues ?

Au bout d’un certain temps, le résultat semble clair. Sur les données d’entraînement, le réseau atteint presque 100 % de réussite. Mais lorsqu’on lui présente les opérations gardées de côté, il échoue. Dans certaines expériences, ses performances restent pratiquement au niveau du hasard.[^1]

***Il a donc appris quelque chose, évidemment. Mais quoi ?***

Alethea Power propose dans sa conférence une comparaison scolaire très parlante. C’est un peu comme un élève qui sait répondre que 6 + 4 = 10 parce qu’il a appris cette association, mais qui ne saurait pas réellement effectuer une addition nouvelle. Le réseau réussit les exemples rencontrés sans disposer encore d’une procédure suffisamment générale pour réussir ailleurs.[^2]

À ce stade, il est en situation de surapprentissage : il réussit presque parfaitement sur les données d’entraînement, mais ne généralise pas encore.

Normalement, l’histoire pourrait s’arrêter ici. Si le réseau réussit parfaitement l’entraînement mais continue d’échouer sur les données nouvelles, pourquoi continuer ?

***C’est précisément à ce moment que survient l’accident.***

Lors de sa conférence, Alethea Power raconte : « Et puis un jour, nous avons eu de la chance. » Elle précise aussitôt, avec humour : « Par chance, je veux dire : par oubli. » Un membre de l’équipe était parti en vacances en oubliant d’arrêter une expérience. Le réseau avait donc continué à s’entraîner pendant une semaine sur les mêmes données.[^2]

***À son retour, quelque chose avait changé.***

Le réseau connaissait déjà presque parfaitement ses exemples d’entraînement. Aucun nouvel exemple ne lui avait été fourni. Pourtant, après une très longue période sans amélioration de sa capacité à généraliser, ses performances sur les opérations jamais rencontrées avaient brusquement commencé à augmenter.

Dans l’expérience emblématique publiée dans l’article, la réussite sur les données d’entraînement devient presque parfaite avant 1 000 étapes d’optimisation. La réussite sur les données de validation, elle, ne rejoint un niveau comparable qu’aux environs d’un million d’étapes. Entre les deux, le réseau continue donc à être entraîné longtemps après avoir presque parfaitement mémorisé les exemples qui lui ont été fournis.[^1]

***Voilà le paradoxe.***

Extérieurement, si l’on ne regardait que ses résultats sur les données d’entraînement, le réseau semblait avoir fini d’apprendre depuis longtemps. Pourtant, l’optimisation continuait à transformer le modèle. À un moment donné, il ne se contentait plus de réussir les exemples rencontrés : il devenait capable de réussir également les exemples de la même tâche qui avaient été tenus à l’écart.

Les chercheurs reproduisent alors ce comportement sur plusieurs tâches et avec différentes configurations. Ce n’est donc pas seulement l’histoire amusante d’un ordinateur oublié pendant des vacances. C’est un phénomène expérimental reproductible dans certaines conditions.[^1]

***Ils lui donnent un nom : le grokking.***

Le mot vient du roman de science-fiction *Stranger in a Strange Land* de Robert A. Heinlein. Pour les chercheurs, il désigne ici cette situation étonnante dans laquelle la généralisation apparaît très longtemps après que le réseau a déjà mémorisé ses données d’entraînement.[^2]

Il faut cependant rester prudent. Cette expérience ne démontre pas qu’un réseau « comprend » au sens où nous parlons de compréhension humaine. Elle montre quelque chose de plus précis, mais déjà remarquable : la réussite sur les exemples appris et la capacité à généraliser peuvent apparaître à des moments très différents de l’apprentissage.[^1]

***Et cela change notre question de départ.***

Lorsqu’une machine donne la bonne réponse, nous ne savons pas encore jusqu’où va ce qu’elle a appris. Pour le découvrir, il faut quitter les exemples sur lesquels elle a été entraînée et la confronter à des exemples qu’elle n’a jamais rencontrés.

***C’est là que commence la généralisation.***

## Sources

[^1]: Alethea Power, Yuri Burda, Harri Edwards, Igor Babuschkin et Vedant Misra, « Grokking: Generalization Beyond Overfitting on Small Algorithmic Datasets », *arXiv*, 2022. https://arxiv.org/abs/2201.02177

[^2]: Alethea Power, intervention lors des *OpenAI Lightning Talks*, transcription publiée par Girl Geek X. https://girlgeek.io/girl-geek-x-openai-lightning-talks-video-transcript/