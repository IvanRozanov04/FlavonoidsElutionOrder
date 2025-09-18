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

---


- **ILD_results_p1/**  
  ILD results obtained after training on IDB (Part 1).  

---

