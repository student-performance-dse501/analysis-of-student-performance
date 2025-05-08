# analysis-on-student-performance

# 🎓 Student Performance Analysis Based on Parental Education

This project investigates the impact of parental education levels and socioeconomic factors on student academic performance in math, reading, and writing. Using a dataset of 1,000 high school students, we performed exploratory analysis, statistical inference, and a variety of regression models to draw meaningful insights about educational equity.

---

## 📊 Dataset Overview

- **Source**: Kaggle – Students Performance dataset  
- **Observations**: 1,000 students  
- **Features**:
  - `gender`, `race/ethnicity`, `parental level of education`, `lunch`, `test preparation course`
  - `math score`, `reading score`, `writing score`

> No missing values were found in the dataset.

---

## 🎯 Objective

To examine whether a student’s academic performance is influenced by their parent’s level of education, and to what extent other demographic factors contribute.

---

## 🔍 Exploratory Data Analysis (EDA)

- Students with college-educated parents scored higher on average.
- Reading and writing scores showed greater variation by parental education.
- Socioeconomic indicators like **lunch type** and **test preparation** also showed clear performance gaps.

> Visualization tools like violin plots, histograms, and bar charts were used for subgroup comparison.

---

## 📐 Statistical Testing

- **ANOVA** and **Welch’s t-tests** confirmed significant differences in scores across parental education levels.
- **Effect size (Cohen’s d)** showed moderate to strong effects in reading and writing.
- Sub-hypotheses (e.g., master's degree vs high school) were statistically supported.

---

## 🔧 Modeling Approach

| Model Type         | Description                                | R² Score | MSE     |
|--------------------|--------------------------------------------|----------|---------|
| Simple Linear      | Only parental education                    | 0.068    | —       |
| Full Linear Model  | All demographic + academic features        | 0.948    | —       |
| Lasso Regression   | Regularized, feature selection             | 0.156    | 181.02  |
| Elastic Net        | Best regularized model                     | 0.160    | 180.15  |
| Random Forest      | Tree-based, non-linear                     | -0.019   | 218.36  |
| Gradient Boosting  | Boosted ensemble                           | 0.085    | 196.09  |

> Elastic Net outperformed other regularized models using only demographic variables.

---

## ✅ Assumptions and Diagnostics

- **Normality**: Shapiro–Wilk test showed residuals were approximately normal.
- **Linearity & Homoscedasticity**: Residual plots showed no major violations.
- **Multicollinearity**: All VIF scores were < 5, confirming no multicollinearity issues.

---

## 💡 Key Findings

- **Parental education**, especially at bachelor’s or master’s level, has a significant impact on student achievement.
- **Lunch type** and **test preparation** are strong secondary predictors.
- Regularized models validated these predictors using demographic data alone.
- Holistic interventions targeting nutrition, support access, and academic prep can close performance gaps.

---

## 📁 Repository Structure

- `student-performance-eda.ipynb` – Complete Jupyter Notebook with analysis
- `project_report_dse501.pdf` – Final academic report (12+ pages)
- `project_slides_dse501.pdf` – Slide deck summarizing the project
- `StudentsPerformance.csv` – Original dataset (1,000 student records)
- `README.md` – Project overview and documentation (this file)

---

## 📚 References

- Brew et al. (2021). *A Literature Review of Academic Performance...*
- Nawang et al. (2021). *A Systematic Literature Review on Student Performance Predictions*
- Wang (2023). *Kaggle Notebook on Parent's Education and School Performance*

---

## 🤝 Authors

Team 43  
*Mitali Kamal Bagadia — ASU ID: 1234311613*  
*Kruthika Suresh — ASU ID: 1233969895*  
*Aditya Rallapalli — ASU ID: 1236173642*  
*Sharan Kumar Varma Chekuri — ASU ID: 1234208003*
