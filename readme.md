
# This model is based on muliple classes classification

## Overview

This documentation details the machine learning model developed to predict student performance based on various features. The model leverages student data to provide insights into factors affecting academic outcomes. Key aspects covered include the challenges faced, methodology used, results, and visualizations.

## Goals

The primary goal of the model is to accurately predict the Grade Point Average (GPA) of students based on a range of demographic, social, and academic factors. The secondary goal is to identify significant predictors of student performance to inform educational interventions.

## Challenges

1. **Data Quality**: Handling missing and inconsistent data was a major challenge. Ensuring data completeness and accuracy was crucial for model performance.
2. **Feature Selection**: Identifying the most relevant features from a large dataset required careful analysis and domain knowledge.
3. **Model Complexity**: Balancing model complexity and interpretability to ensure the model was both accurate and understandable by educators.

## Methodology

1. **Data Collection**: 
    - This dataset contains comprehensive information on 2,392 high school students, detailing their demographics, study habits, parental involvement, extracurricular activities, and academic performance. The target variable, GradeClass, classifies students' grades into distinct categories, providing a robust dataset for educational research, predictive modeling, and statistical analysis.
    - The dataset was downloaded from https://www.kaggle.com/datasets/rabieelkharoua/students-performance-dataset/data

2. **Data Preprocessing**: 
    - **Data Cleaning**: Handled missing values, removed duplicates, and corrected data types to ensure data quality.
    - **Handle Embalanced Data**: The dataset was imbalanced, with some classes having fewer samples. To address this, we used oversampling techniques like SMOTE to balance the class distribution.

3. **Exploratory Data Analysis (EDA)**:
   - **Visualizations**: Histograms, box plots, and scatter plots were used to understand feature distributions and detect outliers.
   - **Statistical Analysis**: Correlation matrix and pairwise correlation plots were used to identify relationships between features.

4. **Model Selection**:
   - Evaluated multiple models: RandomForestClassifier,
        KNeighborsClassifier,
        GaussianNB,
        DecisionTreeClassifier,
        GradientBoostingClassifier,
        XGBClassifier,
        CatBoostClassifier.
   - Used GridSearchCV to tune hyperparameters and optimize model performance.

5. **Model Training and Evaluation**:
   - Split the data into training (80%) and testing (20%) sets using stratified sampling to ensure class distribution consistency.
   - Used 5-fold cross-validation to evaluate model performance and reduce overfitting.

6. **Interpretation and Reporting**:
   - Model's feature importances were extracted to interpret the significance of each predictor.
   - Visualizations were created to present model predictions, feature importances, and performance metrics.

## Results

The final model achieved a cross-validated accuracy of 98.49%. The best performing model used `StandardScaler` for scaling and `RandomForestClassifier` as the classifier. The cross-validation scores demonstrated the model's robustness and high performance.

- **Accuracy:** 100.0%
- **Mean Squared Error:** 0.0
- **Mean Absolute Error:** 0.0
- **R2 Score:** 1.0
- **Cross-validated accuracy:** 0.9849398590159065
- B**est Scaler:** StandardScaler()
- **Best Classifier:** RandomForestClassifier()
- **Best Score:** 1.0

## Visualizations

**1. Feature Correlation Heatmap**
![output2](https://github.com/user-attachments/assets/c1d84888-5624-4583-b2cd-26f43f927c72)

_Description_: The heatmap displays the correlation coefficients between features. High correlations indicate a strong relationship between features, helping in feature selection and understanding multicollinearity.


**2. Confusion Matrix**
![output1](https://github.com/user-attachments/assets/2da57958-f530-4915-872a-6d37148a5836)

_Description_: This plot shows the model’s performance on the testing set, comparing predicted vs. actual GPA values. It displays the number of true positives, true negatives, false positives, and false negatives.


**3. Feature Importance**
![output](https://github.com/user-attachments/assets/172b20da-e0be-40ad-80f0-9fda691961bf)

_Description_: This bar chart ranks features based on their importance in predicting GPA. Features like study time, parental education, and extracurricular activities are shown to be significant predictors.

## Conclusion

The machine learning model developed provides a robust tool for predicting student performance. By addressing data quality issues, carefully selecting features, and optimizing model parameters, the model offers valuable insights into the factors influencing academic success. These insights can guide educators and policymakers in designing targeted interventions to improve student outcomes.
