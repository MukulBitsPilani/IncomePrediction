# IncomePrediction - Model Comparison
Creating a Repo to explore - Adult Income Dataset, Various Mechanism of Data Pre-processing, Implementing key Classification Models and Evaluation Metrics

## Problem Statement:
Predict whether an individual's annual income exceeds `$50K` (`>50K` -> `1`, `<=50K` -> `0`) using demographic and employment features, while comparing five classification models under leakage-free preprocessing.

## Dataset Description
- **Source:** UCI Adult Income dataset (`test_data.csv`), binary classification target (`<=50K` vs. `>50K`).
- **Features & Cleaning:** Dropped `fnlwgt`; converted `?`/`Missing` placeholders to `NaN`; imputed categorical missing values with `"Unknown"` and numerical missing values with the training median.
- **Train-Test Split & Pre-processing:** Stratified `train_test_split` (`test_size=0.2`, `random_state=42`) before one-hot encoding (`OneHotEncoded`, `sparse_output=False, handle_unknown="ignore"`) and `StandardScaler` fit strictly on `X_train` (`.transform()` only on `X_test`).


## GitHub Repository Link
`https://github.com/MukulBitsPilani/IncomePrediction` *(contains training/evaluation script, visualizations, and README)*



## Execution Instructions
1. Open Jupyter Notbook
2. Make sure needed packages are installed.
3. Restart kernel and run all cells top-to-bottom
4. Feel free to play with model parameters like For KNeighborsClassifier you can change the value of n_neighbors, For LogisticRegression you can play with max_iter and without random_state.


   

## Models Used & Evaluation
<img width="779" height="148" alt="image" src="https://github.com/user-attachments/assets/cfbb383a-9191-459c-8223-55f69f7ef221" />


### Graph Representation
- **Dataset Visualizations:**

- 1. Target class distribution countplot:
<img width="469" height="394" alt="image" src="https://github.com/user-attachments/assets/b05e5833-27af-499f-8f56-58fe43c51b30" />


-  2. `hours-per-week` boxplot by income:
<img width="479" height="389" alt="image" src="https://github.com/user-attachments/assets/6dedc6fb-2d20-4125-b414-701db26a23ec" />


-  3. Top 5 `marital-status` stacked proportion chart.
 <img width="557" height="386" alt="image" src="https://github.com/user-attachments/assets/a05c7159-8bea-4cac-94f9-bba439171eb8" />


- **Model Comparison Graph:** Grouped bar chart comparing Accuracy, AUC, Precision, Recall, F1, and MCC across all five models
  <img width="952" height="476" alt="image" src="https://github.com/user-attachments/assets/0f3690ff-6b7f-427d-bbe2-e7993d6de1cb" />

### Model Performance Observations
<img width="487" height="398" alt="image" src="https://github.com/user-attachments/assets/974261dd-b752-406e-ad72-7591ba1d9de1" />
