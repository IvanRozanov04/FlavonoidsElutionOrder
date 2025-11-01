### Fingerprint Generation Workflow
<img width="4195" height="534" alt="Asset 30" src="https://github.com/user-attachments/assets/4eec1212-3ee7-4d89-9752-fb6d99ded62f" />


1. **Applied only to IDB**  
   The entire ILD dataset was used for training; this step applies only to the Internal Database (IDB).

2. **Stratify dataset by retention time**  
   Performed using the `get_retention_time_class(...)` function, which assigns each retention time (RT) to a class used for dataset stratification.

3. **Align atom numbering**  
   Performed using the `reindex_to_mcs(...)` method from the `KernelFPGenerator` class.  
   This function reindexes atoms in the `rdkit_mol` object to ensure consistent numbering across molecules.

4. **Extract substituent information**  
   Performed using the `get_sub_dict(...)` function on the reindexed molecules.  
   This generates a *substituent dictionary* containing information on both substituent positions and compositions.

5. **Generate fingerprints**  
   Performed using `FirstDegreeFP(...)` or `SecondDegreeFP(...)`, which generate a binary fingerprint for each molecule in the dataset.

→ **To ML part…**


The content is organized into two main sections: **Code**, **Data**

---

## 1. Code

This section contains all scripts and notebooks used for model training, evaluation, and visualization.  

### 1.1 Modules
The `Modules/` directory is divided into the following parts:

- **HelperFunctions.py**  
  Utility functions for data aggregation and visualization, shared across models.  

- **FingerPrints/**  
  Functions for generating the custom fingerprints used in this study.  

- **LinearModels/**  
  Includes:  
  - Data pipeline for linear models  
  - Nested cross-validation  
  - Evaluation tools  

- **NeuralNetworks/**  
  Contains two subdirectories:  
  - **BCELoss/** – Models trained with Binary Cross-Entropy loss  
  - **MRLoss/** – Models trained with Margin Ranking loss  

  Each subdirectory includes:  
  - Model implementation  
  - Data pipeline  
  - Cross-validation setup  

---

### 1.2 Jupyter Notebooks
Six notebooks illustrate model implementations, fingerprint workflows, and result analysis:

- **LinearRegression.ipynb** – Linear regression training and statistics aggregation  
- **LogisticRegression.ipynb** – Logistic regression training and statistics aggregation  
- **NNBCE.ipynb** – Neural network with BCE loss (implementation + statistics)  
- **NNMR.ipynb** – Neural network with MR loss (implementation + statistics)  
- **FingerPrintsOverview.ipynb** – Examples of custom fingerprint workflows  
- **Vis&Stats.ipynb** – Aggregated results, visualizations, and statistical testing  

---

## 2. Data

This section contains the datasets used in the study:  

- **IDB.csv** – Initial Database (IDB)  
- **ILD.csv** – Independent Literature Data (ILD)  

