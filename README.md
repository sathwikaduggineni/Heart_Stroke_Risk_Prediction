# Heart_Stroke_Risk_Prediction

This project replicates Akinwumi et al. (2025) *Evaluating machine learning models for stroke prediction based on clinical variables*. It predicts stroke risk using clinical, demographic, and lifestyle features with multiple machine learning models.

---

## Dataset

- Source: [Kaggle Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)  
- 5,110 records, 12 features  
- Target: `stroke` (binary)  

> **Note:** Download `Stroke Prediction Dataset` from the Kaggle link and rename it to "stroke_data.csv" and upload it to Colab when running the notebook.


- `stroke_data.csv` (5,110 records, 12 features)  
- Target: `stroke` (binary)

---

## Workflow

1. **Preprocessing**  
   - Fill missing BMI (median) and smoking status (mode)  
   - Label encode binary features, one-hot encode multi-class features  
   - Remove `id` column  

2. **Train-Test Split & Scaling**  
   - Stratified 80/20 split  
   - StandardScaler applied to numeric features  

3. **Handle Class Imbalance**  
   - SMOTE applied to training set only  

4. **Models**  
   - Logistic Regression, Random Forest, Gradient Boosting, SVM, KNN  
   - Fixed random seeds and reference hyperparameters  

5. **Evaluation**  
   - Accuracy, Precision, Recall, F1-score, ROC-AUC  
   - Confusion matrices, ROC & Precision-Recall curves  
   - 5-Fold Cross-Validation and paired t-tests vs Logistic Regression  
6.  **Result**
   - Best model selected based on ROC-AUC: Logistic Regression
---

## How to Run in Colab

1. Open the notebook directly in Colab:  
   [Open in Colab](https://colab.research.google.com/drive/1seNNfprY1-l6E5Om6k5EJiz6lVXsqluZ#scrollTo=76FEPNmJVZn)

2. Upload `stroke_data.csv` when prompted.  

3. Run the cells sequentially, all preprocessing, training, evaluation, and cross-validation steps are included.

---

## Reproducibility

- Random seed (`42`) ensures consistent results  
- SMOTE applied only to the training set  
- Preprocessing and hyperparameters follow the reference study  
- Full workflow is implemented in the Colab notebook  

---

## Reference
Akinwumi, P. O., Ojo, S., Nathaniel, T. I., Wanliss, J., Karunwi, O., & Sulaiman, M. (2025). 
Evaluating machine learning models for stroke prediction based on clinical variables. Frontiers 
in Neurology, 16, 1668420
