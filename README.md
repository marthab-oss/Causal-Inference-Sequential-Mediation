# Modeling-Coping-Strategy-Improvement-via-Causal-Inference

## Repository Link

https://github.com/marthab-oss/Modeling-Coping-Strategy-Improvement-via-Causal-Inference

## Description

Prediction based on social, educational and health characteristics

### Task Type

Regression

### Results Summary

#### Best Model Performance
- **Best Model:** GradientBoostingRegressor
- **Evaluation Metric:** R², MSE
- **Final Performance:** R²: 0.806, MSE:0.678

#### Model Comparison
- **Baseline Performance:** ElasticNetCV with R²: 0.837,	MSE: 0.569
- **Improvement Over Baseline:** so -4% in R² but +16% in MSE in comparison to best model
- **Best Alternative Model:** SGD Regressor with R²: 0.839, 	MSE: 0.562

#### Key Insights
- **Most Important Features:** social_support_enhancement, mental_health_score, baseline_cognitive_score 
- **Model Strengths:** minimizes bias, good prediction score
- **Model Limitations:** a filled dataset (as few gaps as possible) is needed, as the model only interpolates and does not fill missing datapoints
- **Business Impact:** predicition accuracy, so important to predict trends out of datasets as the base for decision-making

## Documentation

1. **[Literature Review](0_LiteratureReview/README.md)**
2. **[Dataset Characteristics](1_DatasetCharacteristics/exploratory_data_analysis.ipynb)**
3. **[Baseline Model](2_BaselineModel/baseline_model.ipynb)**
4. **[Model Definition and Evaluation](3_Model/model_definition_evaluation)**
5. **[Presentation](4_Presentation/README.md)**

## Cover Image

<img width="1000" height="700" alt="DAG_stat" src="https://github.com/user-attachments/assets/7660e556-07e3-438c-a393-817479251de6" />
