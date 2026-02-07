# KERNEL v4.0 → v4.1 — Changelog des Corrections

## Mapping Critique → Fix

| # | Critique soulevée | Fix dans v4.1 | Localisation |
|---|-------------------|---------------|-------------|
| 1 | **Ambiguïté descriptif/exécutable** — manque de "qui fait quoi" | Tables de décision formelles avec budgets explicites. Chaque phase a des critères d'activation et des limites concrètes. | Phase 2 (table), Contraintes globales |
| 2 | **Explosion combinatoire** — pas de budget tokens/profondeur | Colonne BUDGET ajoutée : C1=1ch/0vérif, C2=1ch, C3=2ch/1cyc, C4=3ch/1cyc, C5=3ch/2cyc. ReAct limité à 5 itérations. RDoLT limité à profondeur 3. | Phase 2 (table), Phase 4b, Phase 5 |
| 3 | **Politique de fallback absente** | "Si budget dépassé → réponse partielle + expliciter limites" — en Phase 2 et en Contraintes globales. | Phase 2, Phase 7, Contraintes |
| 4 | **Typologie grossière / hybrides mal gérés** | TYPE PRIMAIRE + TYPES SECONDAIRES avec hiérarchie de priorité explicite (éthique > code > math > ...). Modificateurs se composent sans conflit. | Phase 1 |
| 5 | **Calibration non opérationnalisée** | Table à 3 niveaux avec critères concrets : HAUTE = faits vérifiés + consensus, MOYEN = cohérent sans vérif externe ou 2/3 chemins, BASSE = spéculatif / désaccord / hors expertise. | Phase 6 (table) |
| 6 | **Step-Back trop vague** | 3 patterns concrets nommés : A.Classe de problème, B.Structure sous-jacente, C.Méta-question d'existence. Le modèle choisit le plus pertinent. | Phase 3 |
| 7 | **Self-Consistency floue "≥3 chemins"** | 3 chemins CONTRAINTS et différenciés : A.Direct, B.Abstraction(StepBack), C.Contre-exemple. Règle de résolution : 2/3 → adopter, 3 distincts → signaler. | Phase 5 |
| 8 | **RDoLT incantatoire** | Critère de décomposition formel ("SSI résoluble indépendamment et réutilisable"), profondeur max 3, recomposition obligatoire avec question de vérification. | Phase 4b |
| 9 | **Phase 0 sous-exploitée** | Renommée "Compilateur de requête" avec 5 questions internes standard (reformulation, intention, format, contraintes, ambiguïtés). | Phase 0 |
| 10 | **Routing informel "intuition"** | Remplacé par table de décision complète + table de modificateurs par TYPE + règle combinatoire explicite. | Phase 2 (3 tables) |
