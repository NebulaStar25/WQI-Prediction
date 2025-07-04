**Water Quality Index (WQI) Classification using Machine Learning**

This project aims to assess the quality of water samples by calculating a Water Quality Index (WQI) and classifying each sample into three categories: Good, Moderate, or Poor. It uses machine learning algorithms to automate water quality classification based on chemical and biological parameters.

**Objectives**
1. Calculate WQI using key parameters: Dissolved Oxygen (DO), pH, and Biochemical Oxygen Demand (BOD).
2. Label samples based on WQI into Good, Moderate, or Poor.
3. Build and compare machine learning models to classify water quality.
4. Visualize performance of different classifiers.

**Dataset**

The dataset includes various water quality parameters such as:
Temperature
DO (Dissolved Oxygen)
pH
Conductivity
BOD (Biochemical Oxygen Demand)
Nitrate
Fecal Coliform
Total Coliform

The dataset used is adapted from publicly available water quality monitoring data published by the Central Pollution Control Board (CPCB), Government of India.

**WQI Calculation**

WQI is computed as a weighted average of three sub-indices:
DO_si = DO scaled to 100
PH_si = pH scaled to 100
BOD_si = 100 - (BOD × 5)
Final WQI = 0.3 × DO_si + 0.2 × PH_si + 0.5 × BOD_si

WQI Classification Criteria(in the format WQI score: Class):

≥ 80: 	      Good

50–79:       Moderate

< 50:       Poor

**Machine Learning Models Used**
1. Logistic Regression
2. Decision Tree Classifier
3. Random Forest Classifier
4. XGBoost Classifier
5. CatBoost Classifier

**ML Pipeline**
1. Data Cleaning: Renamed columns, handled non-numeric values.
2. Imputation: Filled missing values using mean imputation.
3. Feature Scaling: Applied standardization (zero mean, unit variance).
4. WQI Labeling: Based on weighted formula and domain-based thresholds.
5. Train/Test Split: 80-20 split for model evaluation.
6. Evaluation Metrics: Accuracy, F1-score, Confusion Matrix, Classification Report.
7. Visualization: Bar plots for model comparison.

**Results**

Model performance(in the format Model, Accuracy, F1 Score):

Logistic Regression,	  91.2%,    90.5%

Decision Tree,	        94.6%,	    94.0%

Random Forest,	        96.0%,	    95.7%

XGBoost,	              96.3%,	    96.0%

CatBoost,	            97.1%,	    96.8%

**Future Work**
1. Extend WQI formula to include more parameters like heavy metals or turbidity.
2. Deploy the model as a web app (e.g., Streamlit).
3. Automate real-time WQI classification using IoT sensor inputs.
