# 🫀 Recipient Heart Transplant Outcome Prediction

This project leverages data from the **Donor Heart Study (DHS)** and the **Scientific Registry of Transplant Recipients (SRTR)** to build predictive models for 1-year post-transplant outcomes in heart transplant recipients.

---

## 📌 Objective

Develop a machine learning model to predict **composite outcomes** (death, graft failure, or re-transplantation within 1 year) using both **donor** and **recipient** characteristics.

---

## 📊 Dataset Overview

- **Source**: DHS and SRTR Registry  
- **Observations**: 10,882  
- **Original Features**: 150  
- **Final Features Used**: 86 (as specified by PI)  
- **Target Variable**:  
  - `1` = Negative outcome (death, graft failure, or re-transplant within 1 year)  
  - `0` = No negative outcome  

---

## 🔧 Data Preprocessing

- **Missing Value Handling**:
  - Continuous variables: Mean imputation
  - Categorical variables: Mode imputation
- **Outlier Removal**: Based on EDA and visualizations
- **Feature Engineering**: Combined related categorical features and removed redundant ones
- **Transformation**: Log-transformed skewed features (e.g., CPRA)
- **Multicollinearity**: Removed highly correlated predictors

---

## 🧠 Modeling Techniques

Split: 80% Train / 20% Test  
Models Used:
| Model              | Accuracy | AUC  |
|-------------------|----------|------|
| Logistic Regression | 88%      | 0.80 |
| Lasso Regression    | 82%      | 0.80 |
| Random Forest       | **92%**  | **0.84** |

> 🏆 Random Forest performed best with the highest accuracy and AUC.

---

## 📁 Repository Structure

```bash
📦 TransplantMatch--Predicting-Recipient-Outcomes/
├── mainstan.Rmd                 # Main analysis script in RMarkdown
├── stan2.Rmd / stan3.Rmd        # Additional/alternate versions
├── Recipient Heart Transplant Presentation.pptx   # Project summary slides
├── README.md                    # Project documentation


## 🚀 Getting Started

1. **Clone the repo**
   ```bash
   git clone https://github.com/TharunByreddy/TransplantMatch--Predicting-Recipient-Outcomes.git
   cd TransplantMatch--Predicting-Recipient-Outcomes
```

You can explore the full modeling report and results below:

[📄 View Full Report](output/Mainstan1.html)

[🌐 View Web Report](https://tharunbyreddy.github.io/TransplantMatch--Predicting-Recipient-Outcomes/output/Mainstan1.html)



