# État d'application de la feuille de route

**Date :** 4 août 2026  
**Série :** « Une phrase dans la machine »

## Livrables réalisés

- Décisions communes verrouillées dans `DECISIONS_EDITORIALES_SERIE.md`.
- Quatre nouveaux manuscrits créés sans écraser les sources.
- Front matter harmonisé et statut placé à `copy-edit`.
- Transitions officielles intégrées.
- Vérification technique et documentaire consignée dans `VERIFICATION_SOURCES_SERIE_LLM.md`.
- Huit liens de la note d'alignement ouverts sans paramètre de suivi ; page ISO vérifiée en complément.
- Pages 11, 12 et 101 du rapport parlementaire extraites et contrôlées visuellement.
- Quatre schémas explicatifs créés au format 1200 × 675, avec palette, marges, typographie et légendes communes.
- Sources historiques conservées intactes.

## Contrôles réussis

| Contrôle | Résultat |
|---|---|
| Longueur hors encadrés et références | P1 1 612 ; P2 1 747 ; P3 1 787 ; P4 1 986 mots |
| Architecture | Sept sections cibles présentes dans chaque article |
| Connecteurs signature | Aucune formule ne dépasse une occurrence par article |
| Pivot attribué | P1 « Très bien. Mais » ; P2 « Regardons précisément » ; P3 « On pourrait objecter » ; P4 « Il faut distinguer » |
| « lundi matin » | Une seule occurrence dans la série, partie 4 |
| Ancienne collection | Aucun renvoi à « fiche 03 », « tiré à part » ou « infographie 4:3 » |
| Traces de montage | Aucun bloc `MATÉRIAU`, `À VÉRIFIER` ou avertissement « ne pas publier » |
| Anthropomorphismes techniques | Aucune occurrence brute de « le modèle/la machine comprend, sait, veut, choisit ou décide » |
| Images locales | Les quatre liens des manuscrits pointent vers des fichiers existants |
| SVG | Les quatre fichiers sont du XML valide et ont été rendus puis inspectés visuellement |
| Markdown | Les quatre articles et les deux documents de suivi sont convertibles en HTML par Pandoc |
| Liens suivis | Aucun paramètre `utm_source=chatgpt.com` dans les manuscrits |

## Contrôles éditoriaux encore humains

La feuille de route demande trois validations qui ne peuvent pas être honnêtement déclarées terminées par la seule réécriture :

- bêta-lecture par une personne non spécialiste, centrée sur les quatre transitions ;
- relecture des parties 1 et 2 par une personne compétente techniquement ;
- relecture à voix haute finale dans les conditions réelles de publication.

Pour cette raison, les manuscrits restent à l'état `copy-edit` avec `editorial_review: pending`. Après ces trois retours et leurs éventuelles corrections, ils pourront passer à `ready`.

## Fichiers de publication

1. `1 _Matrice/article_01_comment_le_texte_arrive.md`
2. `2_Traitement/article_02_un_modele_continue.md`
3. `3_Qui parle/article_03_qui_parle_version_serie.md`
4. `4_Alignement/article_04_aligne_avec_qui.md`
