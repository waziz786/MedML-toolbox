# Local setup

## Requirements

- Python 3.10 or newer.
- Authorized access to the master dataset used by Module 1.
- Enough local storage for the private source CSV and generated handoff tables.

The repository dependencies are listed in `requirements.txt`. A fresh virtual environment is recommended for each course or project.

## Windows PowerShell

```powershell
py -m venv .venv
\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
$env:MEDML_MASTER_DATASET_PATH = "C:\private\master_dataset_new.csv"
$env:MEDML_OUTPUT_DIR = "$PWD\outputs"
jupyter lab
```

If PowerShell blocks activation, use the Python executable in `.venv\Scripts\python.exe` directly or follow the local organization policy for execution policies.

## macOS or Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
export MEDML_MASTER_DATASET_PATH="$HOME/private/master_dataset_new.csv"
export MEDML_OUTPUT_DIR="$PWD/outputs"
jupyter lab
```

Run the four notebooks in numeric order. If a downstream notebook reports that the M1 handoff is missing, finish Module 1 first or point `MEDML_OUTPUT_DIR` at the private directory containing `M1_dataset_for_next_module.csv`.

## VS Code

Install the Jupyter extension, select the `.venv` interpreter, and open the notebooks from the repository root. The notebooks search the current directory and its parents for the repository layout, so the working directory should remain inside this repository.