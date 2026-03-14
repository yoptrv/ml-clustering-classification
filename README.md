# Machine Learning Project: Clustering and Classification

## Project Overview
This project demonstrates the integration of **unsupervised learning** and **supervised learning** in a machine learning workflow.

The dataset used in this project initially does not contain labels. Therefore, the first step is to apply **clustering techniques** to automatically generate labels based on patterns found in the data.

After the clustering process generates cluster labels, these labels are combined with the original dataset. The resulting labeled dataset is then used to build a **classification model** capable of predicting the class based on the available features.

This project showcases how **unsupervised learning can be used to create labels** that are later used in **supervised learning** to build predictive models.

---

## Dataset
The dataset contains several features related to customer transactions, such as:

- Transaction Amount
- Customer Age
- Transaction Type
- Merchant Category
- Location
- and other related attributes.

Since the dataset initially has **no predefined labels**, clustering is used to identify patterns and group similar data points.

---

## Project Workflow

### 1. Exploratory Data Analysis (EDA)
Initial analysis is conducted to understand the dataset.

Steps performed include:

- Displaying dataset preview (`head()`)
- Checking dataset information (`info()`)
- Descriptive statistics (`describe()`)
- Correlation analysis
- Data visualization

---

### 2. Data Preprocessing
Before modeling, several preprocessing steps are applied:

- Handling missing values
- Removing duplicate data
- Dropping unnecessary columns (ID, date, address fields)
- Encoding categorical features using **LabelEncoder**
- Handling outliers
- Feature scaling using **StandardScaler**
- Feature binning for selected numerical features

---

## Unsupervised Learning: Clustering

In this stage, **K-Means Clustering** is applied to group similar data points.

Steps performed:

1. Determining optimal clusters using **Elbow Method**
2. Applying **K-Means Clustering**
3. Evaluating clusters using **Silhouette Score**
4. Visualizing clusters using **Principal Component Analysis (PCA)**

The clustering results produce labels representing different data groups.

---

## Cluster Visualization
To visualize clustering results, **Principal Component Analysis (PCA)** is used to reduce dimensionality into two components.

This helps visualize how clusters are distributed and where the centroids are located.

---

## Supervised Learning: Classification

After generating cluster labels, the dataset becomes labeled and can be used to train classification models.

Algorithms used in this project include:

- Decision Tree Classifier
- Random Forest Classifier

The dataset is split into:

- **Training Set (80%)**
- **Testing Set (20%)**

using `train_test_split()`.

---

## Model Evaluation

The classification models are evaluated using several metrics:

- Accuracy
- Precision
- Recall
- F1-Score

These metrics measure the model's ability to predict cluster labels correctly.

---

## Hyperparameter Tuning

To improve model performance, **GridSearchCV** is used for hyperparameter tuning.

Parameters optimized include:

- max_depth
- min_samples_split
- min_samples_leaf

---

## Technologies Used

This project uses the following libraries:

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Yellowbrick
- Joblib

---

## Project Structure
ml-clustering-classification
│
├── data
│ └── dataset.csv
│
├── notebooks
│ └── clustering_classification.ipynb
│
├── models
│ ├── model_clustering.h5
│ ├── PCA_model_clustering.h5
│ ├── decision_tree_model.h5
│ ├── explore_RandomForest_classification.h5
│ └── tuning_classification.h5
│
└── README.md


---

## Conclusion

This project demonstrates that:

- **Clustering can generate useful labels** for unlabeled datasets.
- These labels can be used to build **classification models**.
- Combining **unsupervised and supervised learning** provides a powerful approach for data analysis and predictive modeling.

---

## Author

Dio Putra
Machine Learning / Data Science Enthusiast
