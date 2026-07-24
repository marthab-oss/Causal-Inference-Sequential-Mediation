# Dataset Characteristics

**[Notebook](exploratory_data_analysis.ipynb)**

## Dataset Information

### Dataset Source
- **Dataset Link:** https://www.kaggle.com/datasets/cloverchen/causalpitfalls-benchmark-causal-data-neurips-2025
- **Dataset Owner/Contact:** Dataset from Kaggle, no author provided

### Dataset Characteristics
- **Number of Observations:** 500
- **Number of Features:** 8
- **Data Type:** all variables are numerical (int64)

### Target Variable/Label
- **Label Name:** 'coping_strategy_improvement'
- **Label Type:** Regression
- **Label Description:** The target variable represents an individual's ability to adapt to problems or new environments. It is influenced by social, educational, and health-related characteristics.
- **Label Values:** range: 0.18 - 10.80
- **Label Distribution:** The target variable follows an approximately Gaussian distribution, with most observations within the range of of 4 and 8

### Feature Description
all features have the same data type: int64

- **Feature 1 ('educational_intervention'):** Indicates whether additional educational support was provided (binary treatment variable).
  Range: 0-1
- **Feature 2 ('social_support_enhancement'):** Represents additional governmental or social support available to families.
  Range: 0.49 - 16.45
- **Feature 3 ('mental_health_score'):** Measures psychological stability and resilience.
  Range: 66.98 - 238.63
- **Feature 4 ('socioeconomic_status'):** Represents purchasing power related to social status.
  Range: 3.24 - 3.85 
- **Feature 5 ('school_quality_score'):** Measures school quality based on factors such as cancelled lessons, student-teacher relationships, motivation, and available resources.
  Range: 53.22 - 112.61
- **Feature 6 ('baseline_cognitive_score'):** Represents cognitive abilities, including logical reasoning, memory, attention, and processing speed.
  Range: 59.98 - 156.02
- **Feature 7 ('random_noise'):** Randomly generated variable without meaningful influence on the outcome.
  Range: -2.93 - 3.24

## Exploratory Data Analysis


The exploratory data analysis is conducted in the [exploratory_data_analysis.ipynb](exploratory_data_analysis.ipynb) notebook. The analysis includes:

- Data loading and initial inspection
- Statistical summaries and distributions:
  <img width="1200" height="1200" alt="Histogramm" src="https://github.com/user-attachments/assets/51552bf5-8c94-4639-9cfe-05cdc1cd69e8" />
  
- Feature correlation analysis:
 <img width="640" height="480" alt="Correlation_Matrix (1)" src="https://github.com/user-attachments/assets/b0b56ce2-547f-46e2-bb5f-f4588d7f334e" />
 
- Data visualization and insights, like outliners:
  <img width="800" height="400" alt="Boxplot_for_outliners" src="https://github.com/user-attachments/assets/56c2a0f2-8773-4fb9-86f3-79e327bb0d1f" />

- Data quality assessment for data quality, potential biases, and causal analysis challenges:
- Missing value analysis: no missing values detected in dataset
- Selection Bias: The treated group ('educational_intervention' = 1) shows higher baseline values compared to the control group. This is indicated by standardized mean differences (SMD) (particularly for: 'social_support_enhancement': SMD = 0.748 and 'mental_health_score': SMD = 0.575). These differences suggest potential selection bias, as treatment assignment is not completely independent of observed characteristics.
- Predictive Influence: Feature importance analysis shows that 'social_support_enhancement' has the strongest predictive influence on 'coping_strategy_improvement'. It dominates both: ElasticNetCV regression (coefficient β = 0.28) and Gradient Boosting model (feature importance = 0.82)
- Heterogeneous Treatment Effects: The estimated Conditional Average Treatment Effect (CATE) distributions from T-Learner and Random Forest T-Learner range approximately between -3 and +2. This indicates that the effect of the 'educational intervention' varies across individuals, suggesting heterogeneous treatment effects.
- Validation: The `random_noise` feature showed approximately zero predictive influence, confirming that the models are not relying on artificial noise variables.
