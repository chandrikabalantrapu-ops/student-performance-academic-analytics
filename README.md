# student-performance-academic-analytics
Student Performance and Academic Analytics using Python, Pandas and Data Visualization.
# Student Performance & Academic Analytics

## Project Overview

This project analyses student academic performance using Python and Data Science techniques. It explores relationships between student characteristics, study habits, educational support and examination results.

The project also develops machine learning regression models to estimate students' final mathematics grades based on previous academic performance.

## Problem Statement

Understanding student academic performance can help educators identify patterns, examine factors associated with examination results and make informed academic support decisions.

This project investigates:

- What factors are associated with final student grades?
- How are study time and absences related to academic performance?
- How do previous examination grades relate to final grades?
- What patterns can be observed across different student groups?
- Can machine learning estimate final grades using previous examination results?

## Dataset

**Source:** UCI Machine Learning Repository – Student Performance Dataset

Dataset: Student Performance in Mathematics (`student-mat.csv`)

Dataset link: https://archive.ics.uci.edu/dataset/320/student+performance

Dataset details:
- Student records: 395
- Variables: 33
- Missing values: 0
- Duplicate records: 0

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Statsmodels
- Google Colab
- GitHub

## Project Workflow

1. Dataset collection and loading
2. Data inspection and quality checks
3. Exploratory Data Analysis (EDA)
4. Statistical analysis
5. Correlation analysis
6. Data visualisation
7. Student performance categorisation
8. Multiple Linear Regression
9. Model evaluation and comparison
10. Cross-validation

## Key Findings

- Average final mathematics grade (G3): 10.42 out of 20.
- G2 had a strong positive correlation with G3 (0.905).
- G1 had a strong positive correlation with G3 (0.801).
- Previous class failures showed a negative correlation with G3 (-0.360).
- Study time showed a weak positive correlation with G3 (0.098).
- Absences showed almost no linear correlation with G3 (0.034).

### Student Performance Segmentation

Students were grouped using illustrative grade thresholds:

- Needs Support: G3 below 10
- Average: G3 from 10 to below 15
- Good: G3 from 15 to 20

Distribution:
- Needs Support: 130 students
- Average: 192 students
- Good: 73 students

These categories are project-defined analytical segments, not verified institutional grading classifications.

## Machine Learning

Linear Regression was used to estimate final mathematics grades.

### Model Comparison

Two models were evaluated:

**Model A:**
- G1
- G2

**Model B:**
- G1
- G2
- School support
- Family support
- Paid classes
- Internet access

### Test Set Results

| Metric | Model A | Model B |
|---|---:|---:|
| MAE | 1.262 | 1.353 |
| RMSE | 2.052 | 2.126 |
| R² | 0.795 | 0.779 |

### Cross-Validation

Five-fold cross-validation results:

- Model A average R²: 0.827
- Model B average R²: 0.828

Model A was selected as the preferred candidate based on its better held-out test performance and simpler feature set. Cross-validation performance was nearly identical between the models.

## Limitations

- The dataset contains only 395 student records.
- The analysis uses observational data and cannot establish causal relationships.
- The selected model uses G1 and G2, so it is intended for predictions after the second assessment.
- Further validation on independent datasets is required.
- Regression diagnostic checks indicated departures from residual normality.

## Future Improvements

- Explore additional machine learning algorithms.
- Perform more extensive feature engineering.
- Investigate student performance patterns using clustering.
- Develop an interactive academic analytics dashboard.
- Evaluate models on additional student datasets.

## Project Structure

```text
student-performance-academic-analytics/
│
├── data/
│   ├── student-mat.csv
│   └── README.md
│
├── notebooks/
│   └── student_performance_analysis.ipynb
│
├── images/
│   └── performance_charts/
│
├── src/
│
├── README.md
│
└── requirements.txt
```

## Author

Chandrika Balantrapu

Aspiring Junior Data Scientist | Mathematics Educator transitioning into Data Science

Skills: Python | Pandas | NumPy | Machine Learning | Data Analytics | Excel

This project was developed as part of my Data Science portfolio to apply statistical and analytical concepts to real-world educational data.
