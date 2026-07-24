# Modeling-Coping-Strategy-Improvement-via-Causal-Inference

## Repository Link

https://github.com/marthab-oss/Modeling-Coping-Strategy-Improvement-via-Causal-Inference

## Description

This project investigates the prediction and causal analysis of coping strategy improvement based on social, educational, and health-related characteristics. Using machine learning and causal inference approaches, the project aims to identify important predictors, evaluate predictive performance, and investigate potential treatment effects of educational interventions.

### Task Type

Regression with causal inference analysis.

### Results Summary

#### Best Model Performance
- **Best Model:** GradientBoostingRegressor
- **Evaluation Metric:** R², MSE
- **Final Performance:** R²: 0.806, MSE:0.678

#### Model Comparison
- **Baseline Performance:** ElasticNetCV with R²: 0.837, MSE: 0.569
- **Improvement Over Baseline:** so -4% in R² but +16% in MSE in comparison to best model
  
- **Best Alternative Model:** SGD Regressor with R²: 0.839, MSE: 0.562
- **Comparison to Baseline:** The GradientBoostingRegressor did not outperform the linear baseline model, showing approximately a 4% decrease in R² and a 16% increase in MSE compared to ElasticNetCV.

#### Key Insights
- **Most Important Features:** social_support_enhancement, mental_health_score, baseline_cognitive_score as most influential predictors.
- **Model Strengths:** The models achieve strong predictive performance and capture relevant relationships between social, educational, and health characteristics.
- **Model Limitations:** The models require complete input data and mainly capture patterns within the observed dataset. They are not designed to impute missing values or generalize beyond the available data distribution.
- **Business Impact:** The causal analysis indicates potential selection bias in the treatment assignment and heterogeneous treatment effects, meaning that educational interventions may not affect all individuals equally.   Predictive models can support evidence-based decision-making by identifying relevant factors associated with coping strategy improvement. However, causal methods are required to evaluate whether interventions directly contribute to improved outcomes.

## Documentation

1. **[Literature Review](0_LiteratureReview/README.md)**
2. **[Dataset Characteristics](1_DatasetCharacteristics/exploratory_data_analysis.ipynb)**
3. **[Baseline Model](2_BaselineModel/baseline_model.ipynb)**
4. **[Model Definition and Evaluation](3_Model/model_definition_evaluation.ipynb)**
6. **[Presentation](4_Presentation/Presentation.pdf)**

## Cover Image

<img width="1000" height="700" alt="DAG_stat" src="https://github.com/user-attachments/assets/7660e556-07e3-438c-a393-817479251de6" />
