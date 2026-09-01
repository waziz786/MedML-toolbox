# Private data placement

Do not commit MIMIC-IV data or any row-level derivative to this repository.

For local execution, the simplest private layout is:

```text
data/private/master_dataset_new.csv
```

The `data/private/` directory is ignored by Git. Module 1 can also read an explicit path from `MEDML_MASTER_DATASET_PATH`, which is preferred when the dataset is stored elsewhere. The CSV must be the authorized master dataset expected by the Module 1 notebook.

For Google Colab, keep the CSV in a private Google Drive folder and mount Drive from the notebook. Set `MEDML_MASTER_DATASET_PATH` to the mounted file path before running Module 1. See [docs/colab.md](../docs/colab.md).

Access, training, and data-use requirements are described in [docs/data_access.md](../docs/data_access.md). Do not put PhysioNet credentials, access tokens, or private links in notebook cells or documentation.