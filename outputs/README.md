# Generated outputs

This directory is a local workspace, not a source-data archive. Its contents are ignored by Git because the generated tables may contain row-level or otherwise sensitive derived information.

## Handoff

Module 1 writes:

```text
outputs/M1_dataset_for_next_module.csv
```

Modules 2, 3, and 4 read that file. Set `MEDML_OUTPUT_DIR` when the handoff and generated results should live in a private folder outside the repository.

## Analysis artifacts

Each notebook writes module-specific CSV tables for summaries, model results, thresholds, calibration, cross-validation, curves, feature importance, and explainability as applicable. The exact set depends on the notebook version and the data available at execution time.

Do not upload this directory to a public repository, attach row-level results to issues, or place generated files in presentation source control without checking their privacy implications.