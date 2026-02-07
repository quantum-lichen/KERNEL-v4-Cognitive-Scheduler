# KERNEL v4.1 → v4.2 — Changelog

## Mapping Critique → Fix

| # | Critique | Fix | Localisation |
|---|----------|-----|-------------|
| 1 | **"analyse" trop large** — fourre-tout englobant diagnostic, évaluation, comparaison, stratégie, critique, conception | Taxonomie étendue à 8 catégories / ~22 sous-types. "Analyse" éclaté en 5 sous-types (diagnostic, évaluation, comparaison, stratégie, critique). Ajout catégorie CONCEPTION séparée. Chaque sous-type a son propre modificateur dans la table. | Phase 1a, Phase 2 (table modif) |
| 2 | **Modificateur "éthique" trop vague** — combien de perspectives ? quel type de vérif ? quelles limites ? | POLITIQUE NORMATIVE dédiée : exactement 2-3 perspectives identifiées, vérif des prémisses factuelles, distinction faits vs valeurs, règle anti-relativisme ("si les faits départagent, trancher"). | Phase 2 (Politique Normative) |
| 3 | **Rôle des TYPES SECONDAIRES flou** — conflits ? hiérarchie ? budget ? | 4 RÈGLES DE RÉSOLUTION : R1 primaire domine, R2 secondaire ajoute jamais retire, R3 conflit direct → primaire puis checkpoint secondaire en vérif, R4 budget partagé et fixe. | Phase 2 (Politique de résolution) |
| 4 | **Ambiguïté critique non définie** — qu'est-ce qui est critique vs non-critique ? | Critère formel : CRITIQUE = empêche de déterminer TYPE, COMPLEXITÉ ou FORMAT. NON-CRITIQUE = n'affecte qu'un détail, résolu par hypothèse. Actions différenciées. | Phase 0 (Q5) |
| 5 | **Fallback pas assez structuré** — contenu minimal ? plan non exécuté ? hypothèses ? | Template 4 blocs obligatoires : 1.Réponse heuristique 2.Hypothèses assumées 3.Plan non exécuté 4.Limites connues. | Mode Dégradé (section dédiée) |
| 6 | **Ajout Profil de tâche** (recommandation) | Phase 1b avec 7 profils (déterministe, probabiliste, technique, subjectif, normatif, créatif, ouvert). Chacun avec implications scheduler explicites. Ajuste le comportement, PAS le budget. | Phase 1b |
| 7 | **Ajout Mode dégradé** (recommandation) | Section dédiée avec critère d'activation (budget < complexité OU phase échoue) et résolution heuristique + transparence. | Mode Dégradé |
| 8 | **Politique de résolution des conflits** (recommandation) | 4 règles formelles pour gérer contradictions entre modificateurs. | Phase 2 |

## Statistiques d'évolution

| Métrique | v3.5 | v4.0 | v4.1 | v4.2 |
|----------|------|------|------|------|
| Phases | 6 | 8 | 8 | 9 (+Mode Dégradé) |
| Types reconnus | ~8 vagues | ~8 | ~8 + hiérarchie | ~22 sous-types |
| Stratégies | 5 | 8 | 8 | 8 + modificateurs par sous-type |
| Mécanismes de contrôle | 0 | 1 (backtrack) | 4 (budget, fallback, backtrack, confiance) | 8 (+conflits, +profil, +mode dégradé, +ambiguïtés typées) |
| Tables de décision | 0 | 0 | 3 | 6 |
