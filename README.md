# Patterns of Variation Among Baseline Femoral and Tibial Cartilage Thickness and Clinical Features
## Data from the Osteoarthritis Initiative

This repository holds the data-analysis pipeline to reproduce the results and figures in our forthcoming article, "Patterns of Variation Among Baseline Femoral and Tibial Cartilage Thickness and Clinical Features: Data from the Osteoarthritis Initiative" (Keefe, Minnig, Arbeeva, Niethammer, Xu, Shen, Chen, Nissman, Golightly, Marron, Nelson). 

The analysis workflow is presented here as a series of Jupyter notebooks, each of which completes a step of the workflow:

* `01_process_clinical_data.ipynb`: Processes the raw clinical data from OAI, including variable selection, creation of derived variables, and data cleaning.
* `02_standardize_clinical_data.ipynb`: Standardizes most of the (cleaned) numeric clinical variables using the Automatic Shifted Log procedure.
* `03_merge_data.ipynb`: Merges and aligns the three data blocks: clinical variables, femoral cartilage maps, tibial cartilage maps; and produces the two folds of data. After this step the data is ready to be input ot AJIVE.
* `04_fit_ajive_fold1`: Fits the AJIVE model to the Fold 1, and creates the relevant figures. 

Please contact Thomas Keefe to discuss access to the raw data to reproduce our analysis.

It is expected that this workflow will be run in a [`conda`](https://docs.conda.io/projects/conda/en/latest/user-guide/concepts/data-science.html) environment. If conda is installed, this environment can be set up by navigating to your clone of this repository, and using

```
conda env create --file environment.yml
```

The `LICENSE` file defines the license for the data-analytic code in this repository, as software, and does not apply to any published articles related to it.