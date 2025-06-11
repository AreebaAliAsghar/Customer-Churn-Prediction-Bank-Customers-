# Customer Churn Prediction

## Objective
Predict which bank customers are likely to leave (churn), using historical customer data. This analysis helps banks proactively manage customer retention strategies.

## Dataset
- Source: [Kaggle - Churn Modelling Dataset](https://www.kaggle.com/datasets/shubhendra21/churn-modelling-dataset)
- The dataset contains customer demographics and account details, including:
  - CreditScore, Geography, Gender, Age, Tenure
  - Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary
  - Exited (target variable: 1 = churn, 0 = retain)

## Approach
1. **Data Cleaning & Preparation**  
   - Dropped irrelevant columns: RowNumber, CustomerId, Surname.  
   - Handled categorical features:  
     - Gender: Label Encoding  
     - Geography: One-Hot Encoding (dropped first to avoid multicollinearity).  

2. **Exploratory Data Analysis (EDA)**  
   - Visualized features such as credit score, balance, and geography.  
   - Checked class balance in churn variable.

3. **Feature Engineering**  
   - Transformed ‘3+’ in Dependents to numerical 3 (if applicable).  
   - Prepared feature matrix (X) and target (y).  

4. **Modeling**  
   - Used Logistic Regression as a baseline classification model.  
   - Trained on 80% of the data and tested on the remaining 20%.

5. **Evaluation**  
   - Assessed model performance using accuracy and confusion matrix.  
   - Visualized confusion matrix for easier interpretation.

6. **Feature Importance**  
   - Analyzed Logistic Regression coefficients to understand feature impact on churn.

## Results
- Logistic Regression achieved an accuracy of **81%** on the test set.  
- Key features influencing churn include:
  - Age and balance (higher values correlate with higher churn risk).
  - Credit score also impacts churn likelihood.
  - Geography and gender have measurable, but lesser, impact.

## Key Insights
- Older customers and those with higher account balances are more likely to churn.  
- Geography and gender show moderate influence on churn.  
- Logistic Regression provides a good starting point, but other models (like Random Forests or XGBoost) could improve predictions further.

## Conclusion
This project demonstrates the ability to identify customers at risk of churning, enabling banks to tailor strategies for customer retention. Future improvements could include:
- Exploring advanced models for higher predictive accuracy.  
- Adding more domain-specific features or interaction terms.  
- Testing strategies to mitigate churn for high-risk segments.

## References
- Dataset: [Kaggle - Churn Modelling Dataset](https://www.kaggle.com/datasets/shubhendra21/churn-modelling-dataset)
- pandas: [pandas Documentation](https://pandas.pydata.org/docs/)
- seaborn: [seaborn Documentation](https://seaborn.pydata.org/)
- matplotlib: [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- scikit-learn: [scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)

