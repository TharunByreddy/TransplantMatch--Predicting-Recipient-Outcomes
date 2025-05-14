🫀 Recipient Heart Transplant Outcome Prediction
This project leverages data from the Donor Heart Study (DHS) and the Scientific Registry of Transplant Recipients (SRTR) to build predictive models for post-transplant outcomes in heart transplant recipients.

📌 Project Objective
Develop a machine learning model to predict composite outcomes (death, graft failure, or re-transplantation within 1 year) using both donor and recipient characteristics.

📊 Data Overview
Source: DHS and SRTR registry

Observations: 10,882

Original Features: 150

Final Features Used: 86 (as specified by the PI)

Target Variable: Binary (1 = Negative outcome within 1 year, 0 = No negative outcome)

🔧 Data Preprocessing
Missing Value Handling:

Continuous: Mean imputation

Categorical: Mode imputation

Outlier Removal: Based on EDA and visualizations

Feature Engineering:

Combined categorical variables (e.g., race and education)

Created new encoded features

Removed redundant variables

Transformation:

Log-transform applied to skewed features (e.g., CPRA)

Multicollinearity: Highly correlated predictors were removed

🧠 Modeling
Train-Test Split:

80% for training

20% for testing

Models Evaluated:

Logistic Regression

Accuracy: 88%

Lasso Regression

Accuracy: 82%

Lambda optimized via cross-validation

Random Forest

Accuracy: 92%

Best performance (AUC: 0.84)

Model Evaluation:

Used AUC to compare models

Random Forest outperformed others in terms of both accuracy and AUC

📌 Key Learnings
Random Forest handles feature interactions effectively

Proper handling of missing data is crucial (explored mice package and multiple imputation)

Importance of feature selection and transformation

Initial descriptive and EDA are foundational steps in data science

📁 Repository Structure
plaintext
Copy
Edit
├── mainstan.Rmd               # RMarkdown file with full analysis and modeling
├── Presentation1.pptx         # Summary presentation
├── README.md                  # Project overview
├── /figures                   # Visualizations and plots (if applicable)
├── /data                      # Dataset (not included due to privacy concerns)
🚀 How to Reproduce
Clone the repo:

bash
Copy
Edit
git clone https://github.com/your-username/heart-transplant-prediction.git
cd heart-transplant-prediction
Open mainstan.Rmd in RStudio

Install necessary packages:

r
Copy
Edit
install.packages(c("tidyverse", "randomForest", "glmnet", "mice", "ROCR"))
Knit the R Markdown file to generate the report

📚 References
Donor Heart Study (DHS)

Scientific Registry of Transplant Recipients (SRTR)

R Documentation for glmnet, randomForest, mice

