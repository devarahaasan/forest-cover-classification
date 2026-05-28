# 🌿 EcoType: Forest Cover Type Prediction Using Machine Learning

## 📌 Project Overview
EcoType is a machine learning classification project designed to predict the dominant forest cover type in specific geographical areas. By leveraging cartographic variables such as elevation, soil type, slope, and wilderness designations, this project provides an automated, reliable method for environmental monitoring, forestry management, and land-use planning.

---

## 🛠️ Skills Acquired & Demonstrated
* **Exploratory Data Analysis (EDA):** Visualizing complex geospatial and cartographic distributions.
* **Data Cleaning & Preprocessing:** Handling outliers, structural anomalies, and feature skewness.
* **Feature Engineering:** Creating derived distance metrics and encoding high-cardinality categorical data.
* **Classification Model Building:** Implementing and training multiple supervised learning algorithms.
* **Model Evaluation & Hyperparameter Tuning:** Optimizing models using GridSearchCV/RandomizedSearchCV and analyzing confusion matrices.
* **Streamlit App Development:** Designing and deploying a functional web application for real-time model inference.

---

## 🌍 Domain
* Environmental Data Science
* Geospatial Predictive Modeling

---

## 📝 Problem Statement
Accurately mapping forest cover types is essential for ecological research and resource management, but traditional field surveys are resource-intensive. This project solves the problem by building a robust machine learning workflow that automatically classifies forest areas into one of seven distinct cover types using easily obtainable topographic and cartographic features.

---

## 📊 Dataset Details
* **Dataset Size:** 1,45,891 rows × 13 columns
* **Target Variable:** `Cover_Type` (7 distinct classes representing dominant vegetation)

### 📋 Column Descriptions
* **Elevation:** Height above sea level in meters.
* **Aspect:** Slope orientation direction in degrees (0–360°).
* **Slope:** Steepness of the terrain in degrees.
* **Horizontal_Distance_To_Hydrology:** Horizontal distance to the nearest surface water source.
* **Vertical_Distance_To_Hydrology:** Vertical distance to the nearest surface water source.
* **Horizontal_Distance_To_Roadways:** Horizontal distance to the nearest roadway.
* **Hillshade_9am / Hillshade_Noon / Hillshade_3pm:** Relative index of shade/sunlight exposure at specific times (0 to 255).
* **Horizontal_Distance_To_Fire_Points:** Horizontal distance to the closest wildfire ignition point.
* **Wilderness_Area:** Categorical feature indicating the designated regional wilderness area.
* **Soil_Type:** Categorical feature representing the specific soil classification.

---

## 📊 Real-World Use Cases

### 🌲 Forest Resource Management
* Helps forestry departments catalog large timber and conservation zones efficiently without manual surveying.

### 🔥 Wildfire Risk Assessment
* Pairs predicted vegetation types with local climate data to map out and prioritize high-risk fire zones.

### 🗺️ Land Cover Mapping
* Supplies environmental scientists and geospatial analysts with clean data to monitor shifting land usage patterns.

### 🔬 Ecological Research
* Provides structural baselines for biodiversity tracking, soil conservation studies, and wildlife habitat analysis.

---

## 🔧 Project Workflow

### 1. Data Understanding & Preprocessing
* Checked for duplicate entries, missing records, and target class distributions.
* Fixed numeric feature skewness using mathematical transformations (e.g., `log1p`).
* Handled outliers using statistical boundaries (Z-score / IQR).

### 2. Feature Engineering & Selection
* Generated derived interaction variables (e.g., distance ratios and shade variances).
* Applied **SMOTE / RandomOverSampler** to address significant class imbalances.
* Used Random Forest feature importance evaluations to drop low-variance variables.

### 3. Model Building & Optimization
Evaluated five distinct machine learning models to establish performance baselines:
* Random Forest
* Decision Tree
* Logistic Regression
* K-Nearest Neighbors (KNN)
* XGBoost
* **Optimization:** Selected the top-performing model and executed hyperparameter tuning via Grid/Randomized Search.

### 4. Deployment
* Saved the finalized model and associated encoders using `pickle`/`joblib`.
* Built an interactive **Streamlit** user interface allowing manual data entry to output instant, human-readable forest type predictions.

---

## 📂 Repository Structure
```text
├── data/                  # Dataset placeholder or source links
├── saved_models/          # Pickled (.pkl) model and encoder files
├── notebooks/             # Jupyter Notebooks detailing EDA, training, and tuning
├── app/                   # Streamlit web application source code
├── requirements.txt       # List of python dependencies
└── README.md              # Project documentation
