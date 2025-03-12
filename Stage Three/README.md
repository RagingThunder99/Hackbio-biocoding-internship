# Breast Cancer Classification and Clustering

## Overview
This project explores a dataset of breast cancer tumor features to analyze and classify malignant (M) and benign (B) tumors. Using **Principal Component Analysis (PCA)** and **K-Means Clustering**, we attempt to reduce dimensionality and identify patterns in the dataset.

## Dataset
The dataset is sourced from:
[Wisconsin Breast Cancer Dataset](https://raw.githubusercontent.com/PacktPublishing/Machine-Learning-in-Biotechnology-and-Life-Sciences/refs/heads/main/datasets/dataset_wisc_sd.csv)

### Features:
- Various numerical features related to tumor characteristics (e.g., radius, texture, smoothness, concave points, etc.).
- The `diagnosis` column is the target variable (1 = Malignant, 0 = Benign).

## Steps in the Analysis

### 1. Data Preprocessing
- Load the dataset using **pandas**.
- Drop the `id` column (not useful for analysis).
- Convert `diagnosis` to numerical values (M → 1, B → 0).
- Handle missing values by filling them with the column mean.
- Standardize the numerical features using **StandardScaler**.

### 2. Dimensionality Reduction with PCA
- Reduce the dataset to **5 principal components** using **PCA**.
- Analyze the explained variance ratio to determine how much variance is retained.

### 3. K-Means Clustering
- Use the **Elbow Method** to determine the optimal number of clusters.
- Apply **K-Means clustering** with K=2 (to match the number of diagnoses).
- Compare the clusters with actual cancer diagnoses using a confusion matrix.
- Calculate the clustering **accuracy**.

### 4. Visualization
- Visualize PCA-transformed data in **2D scatter plots**.
- Plot clustering results for different values of K (from 2 to 5).

## Results
- The clustering approach groups the tumor samples into distinct clusters.
- The accuracy score helps evaluate how well the clustering matches the true labels.
- Visualizations provide insights into the data distribution.

## Key Learnings
- **PCA** helps in reducing dimensionality while preserving important information.
- **K-Means** can cluster tumors effectively, though it may not be perfect.
- Unsupervised learning techniques like clustering can help in discovering patterns in medical datasets.


# Drug Classification and Docking Score Prediction

## Overview
This project performs exploratory data analysis, feature selection, dimensionality reduction, clustering, and regression modeling on a drug dataset. The dataset contains numerical features related to drug structures, with the goal of predicting the docking score.

## Dataset
- The dataset is loaded from: [drug_class_struct.txt](https://github.com/HackBio-Internship/2025_project_collection/raw/refs/heads/main/Python/Dataset/drug_class_struct.txt)
- Contains various molecular descriptors and a target variable `score` (docking score).

## Key Steps
1. **Data Preprocessing**
   - Non-numeric columns are removed.
   - Missing values are filled with column-wise means.
   - A random sample of 1000 data points is selected for faster processing.

2. **Feature Engineering**
   - Standardization is applied using `StandardScaler`.
   - Feature selection is performed using `SelectKBest` (top 10 features).

3. **Dimensionality Reduction**
   - PCA (Principal Component Analysis) reduces the data to 2 components for visualization.

4. **Clustering Analysis**
   - K-Means clustering is applied with `k=3`.
   - Clusters are visualized using a scatter plot.
   - The average docking score for each cluster is computed.

5. **Predictive Modeling**
   - A `RandomForestRegressor` is trained to predict docking scores.
   - Train-test split (80-20%) ensures proper model evaluation.
   - Model performance is measured using R² score and RMSE.

## Outputs
- PCA-based visualization of chemical space.
- Clustered representation of drugs.
- Mean docking scores per cluster.
- Random Forest model performance (R² and RMSE).

## Results Interpretation
- The lowest docking score cluster represents the most promising drug candidates.
- The predictive model helps estimate docking scores based on molecular descriptors.
