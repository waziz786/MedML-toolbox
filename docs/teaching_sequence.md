# Teaching sequence

## M1: Explore and prepare

Start with the authorized master dataset. Inspect data types, missingness, target construction, and basic ED population patterns. The notebook writes the cleaned handoff file to `MEDML_OUTPUT_DIR`.

## M2: Study length of stay

Use the M1 handoff to describe ED length of stay, examine skew and operational groups, and compare simple classification and regression baselines. Discuss why an outcome should not be imputed as though it were a predictor.

## M3: Model a critical outcome

Reuse the same M1 handoff and focus on patient-level outcome modeling. The notebook compares imbalance-handling strategies and uses patient-disjoint evaluation with `subject_id` groups.

## M4: Model hospitalization and explain it

Reuse the M1 handoff to audit the hospitalization target, compare baseline classifiers, inspect threshold and calibration behavior, and study native feature importance, permutation importance, and SHAP explanations.

## Suggested classroom rhythm

1. Review the matching presentation before running the notebook.
2. Run the data-quality and descriptive sections first.
3. Pause at each modeling decision to identify the target, unit of observation, split strategy, and leakage risks.
4. Compare metrics across models and thresholds rather than selecting a model from one score.
5. Finish by discussing limitations, fairness, generalizability, and the difference between an educational baseline and a clinical tool.