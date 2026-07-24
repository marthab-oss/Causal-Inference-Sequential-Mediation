# Literature Review

Approaches or solutions that have been tried before on similar projects.

**Summary of Each Work**:

- **Source 1**: [Predictive modeling of academic outcomes based on socioeconomic variables]

  - **[Link](https://ceur-ws.org/Vol-4146/short04.pdf)**
  - **Objective**: The study aims to classify students into passing and failing categories based on socioeconomic and educational characteristics.
  - **Methods**: Tree-based ensemble models were applied, including XGBoost, LightGBM, CatBoost, and Explainable Boosting Machine (EBM).
  - **Outcomes**: The models achieved an accuracy of approximately 0.7.
  - **Relation to the Project**: This work is closely related due to the use of similar feature categories, including academic performance, family and parental background, support systems, study habits, and demographic characteristics. However, the study focuses on classification, whereas this project investigates regression-based prediction and causal effects related to coping strategy improvement.

  - **Source 2**: [Using the Bayesian Network Method to Evaluate the Effectiveness of College Students’ Mental Health Intervention Strategies and Their Impact on Academic Performance]

  - **[Link](https://journals.sagepub.com/doi/10.1177/07342829251393575)**
  - **Objective**: The study investigates the prediction of academic performance and psychological risks among students.
  - **Methods**: Bayesian Networks (BN) and Dynamic Bayesian Networks (DBN) were used to model the relationships between psychological factors, interventions, and academic outcomes.
  - **Outcomes**: The models achieved 91.0% accuracy using Bayesian Networks and 94.2% accuracy using Dynamic Bayesian Networks, demonstrating robust prediction under uncertainty.
  - **Relation to the Project**: BN works similar to Directed Acyclic Graphs (DAG), that are used in the project to define causal assumptions. Additionally, both studies investigate intervention effects and relationships between social, psychological, and educational factors.

- **Source 3**: [Machine learning-based academic performance prediction with explainability for enhanced decision-making in educational institutions]

  - **[Link](https://pmc.ncbi.nlm.nih.gov/articles/PMC12290028/)**
  - **Objective**: The study predicts academic performance based on study behavior, previous performance, extracurricular activities, demographic characteristics, and institutional factors such as attendance, teacher quality, and parental involvement.
  - **Methods**: Evaluation of 10 regression models, including K-Nearest Neighbors Regressor, Linear Regression, CatBoost, XGBoost, AdaBoost, and ensemble voting regression. Two datasets containing 10,000 and 6,000 samples were analyzed.
  - **Outcomes**: For the first dataset, the best model achieved an RMSE of 0.1050, MAE of 0.0837, and an R² score of 0.9890. The second dataset achieved an R² score of approximately 0.7.
  - **Relation to the Project**: This study uses similar socioeconomic, educational, and behavioral characteristics. However, it focuses mainly on predictive performance and explainability, while this project extends the analysis by investigating causal relationships and heterogeneous treatment effects.
