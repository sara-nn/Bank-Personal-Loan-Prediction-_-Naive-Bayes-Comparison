Bank Personal Loan Prediction using Naive Bayes
(Machine Learning in Finance - Risk & Customer Behavior Analytics)

This project applies Naive Bayes classification to predict whether a bank customer will accept a personal loan offer, based on demographic and financial attributes. The dataset comes from a bank’s marketing campaign and contains features such as age, income, family size and mortgage.

The main goal is to explore customer data, build predictive models and evaluate their performance to support better decision-making in financial services.

---

    Workflow
1. Data Import & Cleaning
   - Loaded dataset (`Bank_Personal_Loan_Modelling.xlsx`).
   - Checked for missing values, duplicates and inconsistencies.
   - Corrected negative values in the Experience column.

2. Exploratory Data Analysis (EDA)
   - Descriptive statistics with Pandas.
   - Visualizations with Matplotlib and Seaborn (histograms, correlation heatmaps).
   - Insights into customer demographics and loan acceptance patterns.

3. Feature Engineering & Preprocessing
   - Selected relevant variables.
   - Encoded categorical features.
   - Split dataset into training and testing sets.

4. Modeling
   - Trained two Naive Bayes classifiers:
     - GaussianNB
     - MultinomialNB
   - Evaluated using accuracy, confusion matrix and classification report.

5. Results
   - Compared Gaussian vs. Multinomial performance.
   - Identified key predictors (income, education, family size).
   - Demonstrated how predictive analytics can support banking strategy.

---


Languages & Libraries: Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

