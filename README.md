# Telecom Churn Prediction Project

## **Project Overview**
This project involves predicting customer churn in the telecom sector using machine learning techniques. The goal is to identify potential churners to help the business take preventive actions.

---

## **Key Steps Undertaken**

### 1. **Data Loading and Exploration**
   - Loaded the data from CSV files.
   - Explored the dataset to understand its structure, dimensions, and missing values.

   **Challenges Faced**:
   - Missing files or incorrect file paths (e.g., `FileNotFoundError`).
   
   **Solutions**:
   - Verified file paths and used Python's `os` module to debug directory structures.

---

### 2. **Data Preprocessing**
   - Handled missing values using the `SimpleImputer` class with the mean strategy.
   - Standardized column names for consistency.
   - Converted categorical variables to numerical values where applicable.

   **Output**:
   - Cleaned dataset without missing values or inconsistencies.
   - Successfully imputed missing values:
     ```python
     print(X_train_imputed_df.isnull().sum().sum())  # Output: 0
     ```

---

### 3. **Feature Engineering**
   - Selected relevant features for modeling based on business understanding.
   - Scaled the features using StandardScaler.

---

### 4. **Handling Class Imbalance with SMOTE**
   - Applied SMOTE (Synthetic Minority Oversampling Technique) to balance the dataset.

   **Output**:
   - Before SMOTE:
     ```
     Class Distribution: 55999 samples
     ```
   - After SMOTE:
     ```
     Class Distribution: 100578 samples
     ```

---

### 5. **Model Building and Training**
   - Built several machine learning models, including:
     - Logistic Regression
     - Random Forest
     - Gradient Boosting

   - Evaluated models using metrics such as accuracy, precision, recall, and F1-score.

   **Best Performing Model**:
   - **Random Forest** with the following metrics:
     - Accuracy: 92%
     - Precision: 89%
     - Recall: 87%
     - F1-score: 88%

---

### 6. **Challenges Faced**
   1. **Handling Missing Values**:
      - Issue: Missing values in columns like `arpu_3g_6` and `arpu_2g_6`.
      - Solution: Used mean imputation via `SimpleImputer`.

   2. **Imbalanced Classes**:
      - Issue: Target variable was heavily imbalanced.
      - Solution: Applied SMOTE to oversample the minority class.

   3. **File Not Found Errors**:
      - Issue: Incorrect file paths during data loading.
      - Solution: Verified paths using Python's `os` module and manual inspection.

   4. **Model Overfitting**:
      - Issue: Overfitting observed with complex models.
      - Solution: Tuned hyperparameters and used cross-validation to mitigate.

---

### 7. **Key Outputs**
   - Balanced dataset ready for machine learning.
   - Best model with high performance metrics (Random Forest).
   - Insights into customer churn behavior.

---

## **Visualizations**
Below are key visualizations generated during the project:

1. **Feature Correlation Heatmap**  
   ![Feature Correlation Heatmap](https://github.com/Jsan2002/telecom_churn_prediction/blob/main/Graphimg/heatmap.png)

2. **ROC curve**  
   ![ROC curve](https://github.com/Jsan2002/telecom_churn_prediction/blob/main/Graphimg/ROC%20curve%5C.png)

---

## **Future Scope**
1. **Deployment**:
   - Deploy the model as a REST API using Flask/Django.
   - Integrate with real-time systems to predict churn on live data.

2. **Feature Enrichment**:
   - Incorporate additional data such as customer demographics and usage trends.
   - Use external datasets for enhanced predictions.

3. **Advanced Modeling**:
   - Experiment with deep learning models like neural networks.
   - Explore ensemble techniques such as Stacking.

4. **Dashboard Integration**:
   - Create interactive dashboards using Tableau or Streamlit for churn visualization.

---

## **Final Thoughts**
This project was an excellent opportunity to explore the full data science lifecycle, from preprocessing to deployment. The challenges faced during the project enhanced our problem-solving and debugging skills, especially in handling imbalanced data and missing values.

---

## **References**
- [SMOTE Documentation](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.SMOTE.html)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Scikit-learn](https://scikit-learn.org/stable/)

---

## **Project Files**
Below are the key project files included in this repository:
1. `data_dictionary.csv`      - Description of data fields.
2. `telecom_churn.ipynb`      - Jupyter notebook with code and outputs.
3. `telecom_churn_project.md` - This Markdown documentation file.
4. `submission_file.csv`      - submission file for kaggle compitation
---

## **Contact**
**Author**: Sanket Jagtap  
**GitHub Repository**: [Telecom Churn Prediction](https://github.com/Jsan2002/telecom_churn_prediction)  
**Email**: sanketjagtap2002@gmail.com  
