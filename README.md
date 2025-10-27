# 🧠 Dementia Detection Using MRI Data

This project aims to **detect dementia** using clinical and MRI-derived features from the **OASIS (Open Access Series of Imaging Studies)** dataset.  
The goal is to build and interpret machine learning models that can distinguish between healthy individuals and those showing signs of dementia, supporting early diagnosis and research in neurological health.

---

## 📊 Dataset Description

The project uses two open-access datasets from OASIS:

### 🧩 OASIS Cross-Sectional Dataset
- 416 subjects aged 18–96
- Each subject includes MRI and clinical data
- Columns: `ID`, `M/F`, `Hand`, `Age`, `Educ`, `SES`, `MMSE`, `CDR`, `eTIV`, `nWBV`, `ASF`, `Delay`

### 🔁 OASIS Longitudinal Dataset
- 150 subjects with multiple MRI visits
- Tracks cognitive changes over time
- Columns: `ID`, `MRI ID`, `Group`, `Visit`, `MR Delay`, `M/F`, `Hand`, `Age`, `EDUC`, `SES`, `MMSE`, `CDR`, `eTIV`, `nWBV`, `ASF`

**Target variable:** `CDR` (Clinical Dementia Rating)

**Source:** [OASIS Brains — Open Access Series of Imaging Studies](https://www.oasis-brains.org/)

---

## ⚙️ Technologies Used

- **Language:** Python  
- **Libraries:**  
  `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `imbalanced-learn`, `SHAP`, `LIME`
- **Platform:** Google Colab

---

## 🧩 Project Workflow

1. **Data Loading and Preprocessing**
   - Handled missing values
   - Encoded categorical variables
   - Normalized numerical features
   - Addressed class imbalance using **SMOTE**

2. **Exploratory Data Analysis (EDA)**
   - Class and feature distributions
   - Correlation analysis
   - Outlier detection through boxplots and pair plots

3. **Model Training**
   - Models: Logistic Regression, Random Forest, Decision Tree
   - Performance metrics: Accuracy, Precision, Recall, F1-Score, ROC-AUC

4. **Model Evaluation and Interpretation**
   - Confusion Matrix and ROC Curve
   - Feature importance from tree-based models
   - Model explainability using **SHAP** and **LIME**

---

## 📈 Key Visualizations

### 🧩 Class Distribution
Visualizes imbalance between dementia and non-dementia classes before and after balancing with SMOTE.  
![Class Distribution](results/Class distribution.png)

---

### 🔗 Correlation Matrix
Displays relationships between features such as `Age`, `MMSE`, `CDR`, `eTIV`, and `nWBV`.  
![Correlation Matrix](results/Correlation Matrix.png)

---

### 🧮 Confusion Matrix
Shows how well the model classifies dementia vs. non-dementia cases.  
![Confusion Matrix](results/Confusion Matrix.png)

---

### 📉 ROC Curve
Represents model performance in distinguishing between classes.  
![ROC Curve](results/ROC Curve.png)

---

### 🌳 Feature Importance (Random Forest)
Highlights the most influential features for predicting dementia — for instance, `MMSE`, `nWBV`, and `Age`.  
![Feature Importance](results/Feature Importance from random forest.png)

---

### 💡 Model Explainability (SHAP & LIME)
Visualizes how individual features impact specific predictions, demonstrating model transparency.  
![SHAP Explanation](results/SHAP explanation.png)
![LIME Explanation](results/LIME Explanation.png)

---

## 🧠 Results Summary

| Metric | Logistic Regression | Random Forest | Decision Tree |
|:-------:|:-------------------:|:--------------:|:--------------:|
| Accuracy | 0.87 | **0.92** | 0.85 |
| Precision | 0.86 | **0.91** | 0.83 |
| Recall | 0.88 | **0.90** | 0.84 |
| F1-Score | 0.87 | **0.90** | 0.83 |
| ROC-AUC | 0.91 | **0.95** | 0.88 |

✅ **Best Model:** Random Forest Classifier  
✅ **Reason:** High accuracy and interpretability with SHAP/LIME support.

---

## 🚀 Future Improvements

- Incorporate **deep learning** (CNN models) to analyze raw MRI images  
- Apply **hyperparameter tuning** for performance optimization  
- Include **cross-validation** and **ensemble models**  
- Expand to more comprehensive datasets for generalization

---

## 👩‍💻 Author

**Afsana Azad Sarna**  
Project developed as part of Data Science and Machine Learning learning journey.  
Passionate about integrating research and artificial intelligence to contribute to healthcare and neurodegenerative disease studies.

---

## 📚 References

- OASIS Brains — [https://www.oasis-brains.org/](https://www.oasis-brains.org/)  
- Scikit-learn Documentation — [https://scikit-learn.org/](https://scikit-learn.org/)  
- SHAP & LIME for Explainable AI — Lundberg & Lee, 2017  

---

⭐ *If you like this project, don’t forget to give it a star on GitHub!*

