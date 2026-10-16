# Tree Sterility Prediction

## Overview
This project explores whether a tree can be classified as **Sterile** or **Non-Sterile** using biological and environmental features. It was developed for the CSE422: Artificial Intelligence course project and uses Python-based data analysis and machine learning.

## Project Files
- `Tree_Sterility_Prediction.ipynb` — Jupyter Notebook containing data exploration, preprocessing, model training, and evaluation.
- `Tree_Sterility_Prediction_Report.pdf` — Project report describing the dataset, workflow, model comparison, and conclusions.

## Dataset
The project report describes a dataset containing **2,783 rows and 24 features**. The target column is `Sterile`, with two classes:
- Non-Sterile: 2,360 records
- Sterile: 423 records

The dataset is linked in the project report: [Tree Sterility Dataset](https://drive.google.com/file/d/11C-tR5vXotRiA05yq44pubXbIXrzxVTS/view).

The dataset is not included in this repository. Download it from the source above, then update the path in the notebook if necessary. The notebook currently references a Google Drive path:

`/content/drive/MyDrive/422/Tree_Sterility_Dataset.csv`

## Workflow
1. **Exploratory Data Analysis (EDA):** inspect feature types, class balance, correlations, and feature distributions.
2. **Preprocessing:** remove selected columns, handle missing values, encode categorical features, and scale numerical features.
3. **Class balancing and splitting:** the notebook applies SMOTE and uses a stratified train-test split.
4. **Model training:** compare Logistic Regression, Random Forest, K-Nearest Neighbors (KNN), and a Neural Network (`MLPClassifier`).
5. **Evaluation:** compare accuracy, precision, recall, F1-score, confusion matrices, ROC curves, and ROC-AUC.

## Reported Results
The project report records 100% accuracy for Logistic Regression, Random Forest, and the Neural Network, while KNN performs slightly lower (reported around 96.75%–97.03% in different report sections).

These are the results documented in the submitted report; they have not been independently recomputed for this repository. The report also notes that unusually high scores may indicate overfitting or data leakage, so the results should be interpreted cautiously.

## How to Run
The notebook was set up for Google Colab.

1. Upload `Tree_Sterility_Prediction.ipynb` to [Google Colab](https://colab.research.google.com/).
2. Download the dataset from the source link above.
3. Place the CSV in your Google Drive at `MyDrive/422/Tree_Sterility_Dataset.csv`, or edit the dataset path in the notebook.
4. Run the notebook cells in order.
5. If running outside Google Colab, remove or adapt the `google.colab` Drive-mount cell and update the dataset path.

## Requirements
The notebook uses Python and these main libraries:
- pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
- imbalanced-learn

In Google Colab, install any missing packages if prompted, for example:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
```

## Notes
- The notebook includes preprocessing, SMOTE, feature scaling, model comparison, and visual evaluation.
- Ensure preprocessing is fitted only on training data when validating results, and apply resampling only to the training split to avoid data leakage.
- Dataset access may depend on the permissions set by the dataset host.
