# Bank Personal Loan Prediction — Naive Bayes Comparison
(Machine Learning in Finance - Risk & Customer Behavior Analytics)

This project applies **Naive Bayes classifiers** to predict whether a bank customer will accept a personal loan offer. The goal is to demonstrate a complete ML workflow: data cleaning, exploratory data analysis (EDA), model training, evaluation and interpretation.

**Models trained & compared**:
- Gaussian Naive Bayes (GaussianNB)  
- Multinomial Naive Bayes (MultinomialNB)  
- Complement Naive Bayes (ComplementNB)  
- Bernoulli Naive Bayes (BernoulliNB)

## Dataset
- File: `Bank_Personal_Loan_Modelling.xlsx`  
- ~5000 customer records with demographic and financial attributes (Age, Experience, Income, Family, CCAvg, Mortgage, Education...) and target variable Personal Loan.

## Project's steps:
1. **Data import & cleaning**
   - Loaded dataset with pandas.
   - Checked missing values and duplicates.
   - Fixed anomalies (negative values in Experience).
2. **Exploratory Data Analysis (EDA)**
   - Summary statistics, histograms, boxplots, correlation heatmap.
   - Investigated relationships between Income, Education, CCAvg, Family and Personal Loan.
3. **Feature Engineering & Preprocessing**
   - Selected relevant variables.
   - Encoded categorical features.
   - Split dataset into training and testing sets.
4. **Modeling**
   - Trained four Naive Bayes classifiers (Gaussian, Multinomial, Complement, Bernoulli).
   - Evaluated on test set using: **Accuracy**, **F1-score**, **confusion matrix** and classification reports.
5. **Interpretation**
   - Compared model behavior focusing on ability to detect minority class (loan accepted).
   - Noted class imbalance and the effect on accuracy vs. F1.

Languages & Libraries: Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

## Key Results (test set)
| Model | Accuracy | F1-score (test) | Notes |
| GaussianNB | **88.3%** | **0.489** | Best F1 among the four — better at identifying positives than others. |
| MultinomialNB | **80.4%** | **0.410** | Moderate performance. |
| ComplementNB | **77.2%** | **0.384** | Lower recall on minority class. |
| BernoulliNB | **90.4%** | **0.000** | High accuracy but predicted only majority class _ F1=0 for minority (class imbalance issue). |

**Interpretation:** BernoulliNB’s high accuracy is misleading due to class imbalance. GaussianNB provided the best balance (higher F1). For imbalanced targets, prefer metrics like F1, recall or precision-recall curves.
