// ...existing code...
# AI Assignment 4 — README

Notebook: `ai_assign_4.ipynb`  
Location: this folder

## Overview
This Jupyter notebook trains and evaluates simple neural networks on the MNIST dataset. It contains four parts (A–D) that experiment with different network architectures and activation functions, then plots training vs. test accuracy and prints a classification report.

Part highlights:
- Part A: single hidden layer (40 units, ReLU)
- Part B: two hidden layers (20, 20 units, ReLU)
- Part C: three hidden layers (30, 20, 40 units, ReLU)
- Part D: same as C but using sigmoid activations

## Files
- ai_assign_4.ipynb — notebook with code, training, plots and evaluation.
- readme.md — this file.

## Requirements
Recommended Python environment (Windows / PowerShell):
- Python 3.8+
- Packages:
  - tensorflow (or tensorflow-cpu)
  - matplotlib
  - numpy
  - scikit-learn
  - jupyterlab or notebook (optional for running)

Example pip install (adjust tensorflow variant if you need GPU/CPU):
```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install tensorflow matplotlib numpy scikit-learn jupyterlab
```

## How to run
1. Activate the venv in PowerShell:
   ```powershell
   .\.venv\Scripts\Activate.ps1
   ```
2. Open the folder in VS Code and open `ai_assign_4.ipynb`; select the interpreter/kernel from the created venv.
3. Run cells sequentially or run the whole notebook. Alternatively start JupyterLab:
   ```powershell
   jupyter lab
   ```

## Notes & troubleshooting
- The notebook uses Keras' built-in MNIST loader: no external dataset download is required.
- If imports fail, ensure the venv interpreter is selected in VS Code and packages are installed into that environment.
- For large GPU training use the appropriate `tensorflow` package (GPU-enabled) and correct CUDA/cuDNN versions.
- If the kernel doesn't appear, install ipykernel and register the kernel:
  ```powershell
  pip install ipykernel
  python -m ipykernel install --user --name ai_assign4 --display-name "AI Assign 4"
  ```

## Suggested improvements (optional)
- Add a `requirements.txt` with exact versions (use `pip freeze` or `pipreqs`).
- Split repeated training/evaluation code into functions to avoid duplication.
- Save trained models and evaluation outputs to disk for later analysis.
- Add confusion matrix plots for deeper error analysis.
