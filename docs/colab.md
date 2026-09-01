# Google Colab workflow

Colab is convenient for students who cannot install the scientific Python stack locally. The runtime is still user-controlled, so private data can be copied or downloaded by code running in that runtime. Absolute non-downloadability is not possible in standard Colab.

## Start a private working copy

1. Open the repository in GitHub and open a notebook with Colab, or clone the repository into the runtime.
2. Install the public dependencies in a Colab cell:

   ```python
   %pip install -r requirements.txt
   ```

3. Mount the private Drive folder that contains the authorized CSV:

   ```python
   from google.colab import drive
   drive.mount("/content/drive")
   ```

4. Set the data and output paths before running Module 1:

   ```python
   import os

   os.environ["MEDML_MASTER_DATASET_PATH"] = \
       "/content/drive/MyDrive/MedML_Toolbox/master_dataset_new.csv"
   os.environ["MEDML_OUTPUT_DIR"] = \
       "/content/drive/MyDrive/MedML_Toolbox/outputs"
   ```

5. Run the notebooks in order: M1, M2, M3, then M4. Keep the handoff and generated outputs in the private Drive folder if the runtime may be reset.

## Colab privacy checklist

- Do not upload the source CSV to a public GitHub issue, release, gist, or shared notebook.
- Do not store PhysioNet credentials or tokens in notebook cells.
- Do not share a runtime link containing private data.
- Disconnect the runtime and unmount Drive when finished.
- Treat all generated CSVs as sensitive until reviewed.

Students must obtain and use the data only under the applicable PhysioNet and institutional requirements. See [data_access.md](data_access.md).