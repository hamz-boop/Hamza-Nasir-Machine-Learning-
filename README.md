# Random Forest Classification on the Heart Disease Dataset  

## Introduction  
Cardiovascular disease remains the leading cause of death worldwide. Early detection and diagnosis are crucial for effective treatment and improved patient outcomes.  

This project demonstrates a **Random Forest Classifier** applied to the **Heart Disease dataset** to predict the presence of heart disease based on clinical and demographic features. The goal is to create a binary classification model that predicts whether a person will have heart disease (`1`) or not (`0`) with high accuracy.  

The project follows a structured workflow:  
- Data loading and preprocessing  
- Model training and evaluation  
- Advanced visualizations for interpretability  
- Suggestions for improvements  

---

## Dataset Overview  
The dataset used comes from the **UCI Machine Learning Repository** and **OpenML**. It contains **303 records** and **14 attributes** representing clinical and demographic factors.  

### **Features**  
| **Feature** | **Description** |
|------------|----------------|
| age        | Age of the individual in years |
| sex        | Biological sex (0 = female, 1 = male) |
| cp         | Chest pain type (0–3) |
| trestbps   | Resting blood pressure (mm Hg) |
| chol       | Serum cholesterol (mg/dL) |
| fbs        | Fasting blood sugar (>120 mg/dL or not, 0 or 1) |
| restecg    | Resting electrocardiographic results (0–2) |
| thalach    | Maximum heart rate achieved |
| exang      | Exercise-induced angina (0 = no, 1 = yes) |
| oldpeak    | ST depression induced by exercise relative to rest |
| slope      | Slope of the peak exercise ST segment (0–2) |
| ca         | Number of major vessels colored by fluoroscopy (0–3) |
| thal       | Type of heart defect (0–3 or 1–3) |
| target     | Class label (0 = no heart disease, 1 = heart disease) |

### **Shape**  
- **Total samples:** 303  
- **Features:** 13  
- **Target:** 1 (binary classification)  

---

## Objective  
The objective is to develop a Random Forest model that can accurately classify patients into two groups:  
- **0** = No Heart Disease  
- **1** = Heart Disease  

---

## Model Evaluation  
The model is evaluated using the following metrics:  

| **Metric** | **Value** |  
|------------|-----------|  
| **Accuracy** | 79% |  
| **Precision** | 0.79 |  
| **Recall** | 0.84 |  
| **F1-Score** | 0.82 |  

### **Confusion Matrix**  
| Actual/Predicted | No Disease (0) | Disease (1) |  
|------------------|----------------|-------------|  
| **No Disease (0)** | 30 (TN) | 11 (FP) |  
| **Disease (1)** | 8 (FN) | 42 (TP) |  

- The model correctly classified **72 out of 91** test samples.  
- High recall (**0.84**) indicates that the model effectively identifies positive cases (heart disease).  

---

## Visualizations  
### 1. **Confusion Matrix**  
- Heatmap of the confusion matrix using **YlOrBr** colormap.  

### 2. **Pair Plot**  
- Visualizes correlation between key features (e.g., age, cholesterol, maximum heart rate).  

### 3. **Parallel Coordinates Plot**  
- Shows how features like **thalach**, **oldpeak**, and **cp** vary across different classes.  

### 4. **Calibration Curve**  
- Model is reasonably well-calibrated but can be improved at certain probability thresholds.  

### 5. **Feature Importance**  
**Top 3 Important Features:**  
- **cp** (chest pain type)  
- **oldpeak** (ST depression)  
- **thalach** (maximum heart rate)  

### 6. **Single Decision Tree**  
- Extracted from the Random Forest to provide insights into individual decision rules.  

---

## Results and Insights  
✅ **Performance:**  
- **79% accuracy** with balanced precision and recall.  
- Strong recall ensures that most positive cases are correctly identified.  

✅ **Feature Importance:**  
- **Chest pain type** (`cp`) and **ST depression** (`oldpeak`) are the most important predictors.  

✅ **Clinical Relevance:**  
- Model aligns well with medical knowledge.  
- High recall reduces the chance of missing positive cases (false negatives).  

---

## Potential Improvements  
### 🔧 **Hyperparameter Tuning**  
- Optimize **n_estimators**, **max_depth**, and **min_samples_split** using **GridSearchCV** or **RandomizedSearchCV**.  

### 🔁 **Cross-Validation**  
- Implement **K-fold cross-validation** to improve model robustness.  

### 🎯 **Feature Engineering**  
- Create interaction terms or new features from domain knowledge.  

### 🛠️ **Cost-Sensitive Learning**  
- Adjust class weights to reduce false negatives.  

### 🧠 **Explainability Tools**  
- Use **SHAP** and **LIME** for local interpretability.  

---


## Installation  
### Step 1: Clone the repository  
```bash
git clone https://github.com/yourusername/RandomForest-HeartDisease.git


