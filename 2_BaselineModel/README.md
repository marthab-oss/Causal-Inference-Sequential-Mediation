# Baseline Model

[Notebook](baseline_model.ipynb)**

## Baseline Model Results

### Model Selection
- **Baseline Model Type:** ElasticNetCV
- **Rationale:** ElasticNetCV was selected as the baseline model because it combines the advantages of Lasso and Ridge regression. It is suitable for regression problems with multiple potentially correlated features, as expected in this dataset where social, educational, and health characteristics may influence each other. The automatic cross-validation-based selection of regularization parameters also reduces the risk of overfitting, which is important due to the relatively small dataset size (500 observations).


### Model Performance
- **Evaluation Metric:** MSE, MAE, R², RMSE
- **Performance Score:** R²: 0.837, MSE: 0.570, MAE: 0.584, RMSE: 0.755

### Evaluation Methodology
- **Data Split:** [Train/Validation/Test split ratios, e.g., 70/15/15]
- **Evaluation Metrics:** The selected metrics provide different perspectives on regression performance:
  - R² (Coefficient of Determination): Measures the proportion of variance in coping strategy improvement explained by the model. An R² value of 0.837 indicates that the model explains approximately 84% of the variability in the target variable.
  - MAE (Mean Absolute Error): Represents the average absolute prediction error. The MAE of 0.584 means that predictions differ from the actual coping strategy improvement values by approximately 0.58 units on average.
  - MSE (Mean Squared Error): Penalizes larger prediction errors more strongly due to squaring the residuals. This metric helps identify whether the model produces occasional large deviations.
  - RMSE (Root Mean Squared Error): Provides the prediction error in the same unit as the target variable. The RMSE of 0.755 indicates the typical magnitude of prediction errors while placing additional emphasis on larger mistakes.

### Metric Practical Relevance
The evaluation metrics indicate how accurately coping strategy improvement can be predicted based on social, educational, and health characteristics. A high R² value suggests that the selected characteristics contain substantial information about differences in coping strategy improvement. The MAE and RMSE values show the expected prediction uncertainty when estimating an individual's outcome.
In a practical setting, these predictions could support identifying individuals who may benefit from additional educational or social interventions. However, prediction performance alone does not establish causal effects; therefore, further causal inference methods are required to evaluate whether specific interventions actually improve coping outcomes.


## Next Steps
This baseline model serves as a reference point for evaluating more sophisticated models in the [Model Definition and Evaluation](../3_Model/README.md) phase.
