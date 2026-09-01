# Data access and privacy

The notebooks are designed for an authorized, de-identified MIMIC-IV ED-derived master dataset. The dataset itself is intentionally absent from GitHub.

## Before running

Obtain the appropriate access through PhysioNet and follow the current required training, credentialing, data-use agreement, and institutional policies. The course repository does not grant access and does not replace those requirements.

Keep the source CSV in private storage. Use `MEDML_MASTER_DATASET_PATH` to point to it, or place it at the ignored local path `data/private/master_dataset_new.csv`.

## What must stay private

- The authorized master dataset.
- The M1 handoff and all row-level derived CSVs.
- Credentials, tokens, signed URLs, and institutional configuration.
- Notebook outputs that expose individual rows, identifiers, or sensitive derived values.

The repository `.gitignore` excludes the `data/` and `outputs/` contents while preserving their README files. Check `git status` before every commit.

## Colab limitation

Google Colab can mount private Drive storage, but code executing in a user-controlled runtime can read and copy any data that the runtime can access. Therefore this repository can reduce accidental publication, but it cannot guarantee that authorized data is non-downloadable during execution. Use only approved data and approved workflows.

## Reporting results

Share aggregate, reviewed teaching results only. Review plots, tables, notebook outputs, and presentation exports for disclosure risk before distributing them. Do not treat model performance from this curriculum as clinical validation or deployment evidence.