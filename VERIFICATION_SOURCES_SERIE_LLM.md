# Vérification technique et documentaire — Série LLM

**Dernière vérification :** 4 août 2026  
**Manuscrits contrôlés :** parties 1 à 4 de « Une phrase dans la machine ».

## Partie 1 — entrée du texte

| Point contrôlé | Conclusion appliquée au manuscrit | Source primaire |
|---|---|---|
| Tokenisation sous-lexicale | Le découpage dépend du tokenizer ; aucun découpage précis n'est présenté comme universel. | Kudo et Richardson, [SentencePiece](https://aclanthology.org/D18-2012/), 2018 |
| Token, identifiant, plongement | Trois objets séparés ; l'identifiant est un index et non une grandeur sémantique. | Description architecturale cohérente avec Vaswani et al., [Attention Is All You Need](https://arxiv.org/abs/1706.03762), 2017 |
| Position | Le texte ne suppose pas un mécanisme unique : encodage ajouté ou position introduite dans l'attention selon l'architecture. | Vaswani et al., section 3.5 et variantes de la section 6.2 |
| Plongement initial / état contextuel | Le premier appartient aux paramètres fixés ; le second est une activation calculée pour une occurrence. | Vaswani et al., sections 3.1 à 3.3 |
| Métaphore géométrique | Les projections 2D et directions interprétables sont signalées comme simplifications dépendantes du modèle. | Limite formulée comme précaution pédagogique ; aucune mesure fictive n'est attribuée à un modèle réel. |

## Partie 2 — génération

| Point contrôlé | Conclusion appliquée au manuscrit | Source primaire |
|---|---|---|
| Attention causale | Une position peut utiliser sa propre position et les précédentes ; le futur est masqué. | Vaswani et al., section 3.2.3 |
| Flux principal et dimensions intermédiaires | Un état par position est conservé dans le flux résiduel ; les dimensions intermédiaires peuvent différer. | Vaswani et al., sections 3.1 et 3.3 |
| Dernière position | Elle est lue parce qu'elle a accès à tout le préfixe dans un modèle causal, non parce qu'elle serait intrinsèquement privilégiée. | Propriété déduite du masque causal de Vaswani et al. |
| Logits / softmax / probabilités | Les scores non normalisés sont nommés logits ; la softmax produit la distribution. | Vaswani et al., sections 3.2 et 3.4 |
| Partage des poids entrée-sortie | Présenté comme fréquent, jamais universel. | Press et Wolf, [Using the Output Embedding to Improve Language Models](https://arxiv.org/abs/1608.05859), 2016 |
| Sélection | La température et les filtres sont des réglages de la procédure d'inférence ; les tableaux sont explicitement fictifs. | Principe général documenté sans attribuer un réglage à tous les systèmes. |
| Cache KV | La boucle est qualifiée de conceptuelle ; le cache évite de recalculer les états antérieurs sans changer l'ordre autoregressif. | Vérification architecturale ; formulation limitée au principe courant. |

## Partie 3 — modèle de sélection du personnage

Source principale ouverte et relue : Sam Marks, Jack Lindsey et Christopher Olah, [The Persona Selection Model](https://alignment.anthropic.com/2026/psm/), 23 février 2026.

| Point contrôlé | Conclusion appliquée au manuscrit |
|---|---|
| Statut de la source | Hypothèse ou modèle mental proposé par des chercheurs d'Anthropic, non description établie de tous les assistants. |
| Linda–David | Exemple présenté comme une continuation qui exige de représenter les informations et intérêts attribués aux personnages. |
| Post-entraînement | Décrit, selon le PSM, comme un affinage d'une distribution de personas ; l'analogie bayésienne n'est pas prise au pied de la lettre. |
| Désalignement émergent | Le texte sépare le résultat expérimental de l'interprétation PSM. Source d'expérience : Betley et al., [Emergent Misalignment](https://arxiv.org/abs/2502.17424), 2025. |
| Lancer de pièce | Claude Sonnet 4.5 donne 88 % à l'issue associée à la tâche préférée dans l'exemple publié ; le modèle de base reste proche de 50 %. Le résultat fragilise une lecture, sans trancher l'agentivité. |
| Agentivité | Définition fonctionnelle limitée à une conduite orientée vers un but ; volonté subjective et préférence apprise sont explicitement séparées. |

## Partie 4 — huit liens de la note source

Les huit destinations de `4_Alignement/definition explication.md` ont été ouvertes une à une, sans le paramètre `utm_source=chatgpt.com`. La page ISO, absente de la liste numérotée finale mais demandée par la feuille de route, a également été vérifiée.

| Source vérifiée | Proposition effectivement soutenue dans le nouvel article | État au 2026-08-04 |
|---|---|---|
| [International AI Safety Report 2026](https://internationalaisafetyreport.org/publication/international-ai-safety-report-2026) | Les risques et leur gestion reposent sur des preuves encore incomplètes ; la publication est datée du 3 février 2026. | Ouverte |
| [Artificial Intelligence, Values, and Alignment](https://link.springer.com/article/10.1007/s11023-020-09539-2) | Instructions, intentions, préférences, intérêts et valeurs ne sont pas des cibles équivalentes ; des procédures équitables doivent arbitrer. | Ouverte |
| [Cooperative Inverse Reinforcement Learning](https://arxiv.org/abs/1606.03137) | Référence historique sur l'inférence de préférences ; aucune affirmation générale sur le reward hacking ne lui est attribuée. | Ouverte |
| [Aligned with Whom?](https://www.nber.org/papers/w30017) | Distinction entre alignement direct et social, et rôle des externalités et de la gouvernance. | Ouverte |
| [Convention-cadre du Conseil de l'Europe](https://www.coe.int/fr/web/artificial-intelligence/the-framework-convention-on-artificial-intelligence) | Droits humains, démocratie et État de droit sur le cycle de vie ; ouverte à la signature le 5 septembre 2024. | Ouverte |
| [NIST — caractéristiques de confiance](https://airc.nist.gov/airmf-resources/airmf/3-sec-characteristics/) | Caractéristiques sociotechniques, arbitrages contextuels et responsabilité des acteurs. | Ouverte ; AI RMF 1.0 en cours de révision |
| [NIST — AI RMF Core](https://airc.nist.gov/airmf-resources/airmf/5-sec-core/) | Gouverner, cartographier, mesurer et gérer ; gestion continue sur le cycle de vie. | Ouverte ; AI RMF 1.0 en cours de révision |
| [Règlement (UE) 2024/1689](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/fra) | Pour les systèmes à haut risque : contrôle humain (art. 14) et exactitude, robustesse, cybersécurité sur le cycle de vie (art. 15). | Ouverte |
| [ISO/IEC 42001:2023](https://www.iso.org/standard/42001) | Établir, mettre en œuvre, maintenir et améliorer continuellement un système de management de l'IA. | Ouverte |

## Rapport parlementaire local et appels de note orphelins

Le PDF `4_Alignement/Mission-Alignement-IA-Rapport-DEF.pdf` a été extrait puis contrôlé visuellement.

- p. 11 : l'alignement porte sur le système, non le modèle isolé, et articule exigences technique, normative et systémique ;
- p. 12 : définition retenue dans le rapport ;
- p. 101 : impossibilité d'assurer un alignement intégral et objectif d'un alignement effectif, dynamique et vérifiable.

Les quatre appels de note orphelins de la note source ne sont pas repris. Le nouvel article rattache les propositions conservées aux pages 11-12 et 101 du rapport, ou les soutient par une source primaire explicitement listée. Le fichier `definition explication.md` reste intact comme archive.

## Catégories de preuve utilisées

- **Fait ou mécanisme établi :** formulation directe et source primaire.
- **Simplification pédagogique :** signalée dans le texte ou la légende du schéma.
- **Hypothèse interprétative :** attribuée à ses auteurs, particulièrement dans la partie 3.
- **Question normative :** laissée à une autorité ou à une procédure légitime, jamais présentée comme déduite du calcul.
