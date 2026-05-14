LOAN APPROVAL PREDICTION MODEL

Project Overview

This project involves the creation of a synthetic financial dataset and the development of a Linear Regression model to predict loan approval ratings. The goal is to simulate a realistic banking environment where approval is determined by a combination of demographic, financial, and behavioral factors.

1. Data Simulation Logic

To ensure the model learns meaningful relationships, the data was synthesized using Numpy and Pandas with specific conditional logic:

 - Population & Demographics
 - Sample Size: 3,000 synthetic applicants.
 - Age: Applicants range from 21 to 60 years old.
 - Employment Status: Randomly assigned as Employed, Unemployed, or Self-employed.

Financial & Behavioral Features

 - Conditional Profiles: Income and Credit Scores are tied to employment status to mimic real-world correlations (e.g., employed individuals generally have higher income baselines).
 - Debt-to-Income: Calculated by dividing existing debt by annual income.
 - Default History: Derived from a "Payment History" category (Good, Average, Bad), resulting in a discrete count of previous defaults.

2. Exploratory Data Analysis (EDA)

The dataset features were visualized using Matplotlib to confirm logical distributions:

 - Income vs. Score: Showed a positive correlation, where higher income levels generally lead to higher approval ratings.
 - Credit Score vs. Approval: Demonstrated a strong linear relationship, confirming creditworthiness as a primary driver of the model.
 - Defaults vs. Score: Showed a clear "step-down" penalty where each additional default significantly lowers the approval ceiling.

3. Model Architecture

The project utilizes a supervised learning approach:

 - Algorithm: Linear Regression.
 - Features (X): income, credit_score, num_of_defaults, loan_amount, and existing_debt.
 - Target (y): loan_approval_rating.
 - Data Split: 80% Training, 20% Testing.

4. Performance Metrics

The model was evaluated on the unseen test set with the following results:

 - R-squared ($R^2$): ~0.89 (The model explains 89% of the variance in approval ratings).
 - Mean Squared Error (MSE): ~0.0017 (Indicating high prediction precision).

5. Conclusion

The high $R^2$ score and the tight clustering in the Actual vs. Predicted plot confirm that the Linear Regression model is a highly effective tool for predicting loan outcomes based on the simulated financial parameters.