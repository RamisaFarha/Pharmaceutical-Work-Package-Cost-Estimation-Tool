# Pharmaceutical Work Package Cost Estimation Tool

## Overview
The **Pharmaceutical Work Package Cost Estimation Tool** is an AI-driven solution designed to estimate costs for pharmaceutical work packages. This tool leverages machine learning (ML) and natural language processing (NLP) techniques to analyze historical data and predict costs with high accuracy, facilitating resource planning and budget optimization.

---

## Key Features
- **Cost Prediction**: Estimate costs for pharmaceutical work packages based on key parameters (e.g., task type, duration, and resources).
- **Synthetic Dataset Generation**: Create and preprocess synthetic datasets that mimic real-world work package data.
- **ML Model Training and Evaluation**: Train a regression-based ML model for accurate cost prediction.
- **Data Visualization**: Provide insights such as cost vs. duration relationships and feature importance.
- **Real-Time Prediction Interface**: Deploy a user-friendly interface using Streamlit for real-time predictions.

---

## Dataset
**Pharmaceutical Work Package Dataset**:
- **Size**: 5,000 rows
- **Features**:
  - **Task Type**: Type of work package (e.g., Analysis, Development, Testing, Validation).
  - **Resources**: Number of resources allocated to the work package.
  - **Duration**: Duration of the task in days.
  - **Cost**: Cost of completing the task (target variable).

### Synthetic Dataset Generation
- The dataset was generated using random sampling techniques to simulate real-world scenarios.
- Implementation details can be found in the `generate_pharma_dataset()` function within the codebase.

---

## Machine Learning Workflow

### Data Preprocessing
1. **Categorical Data Handling**: One-hot encoding applied to the `Task Type` column.
2. **Feature Scaling**: Numerical features (`Resources`, `Duration`, and encoded `Task Type`) scaled using `StandardScaler`.

### Model Training
- **Model**: Random Forest Regressor (from `scikit-learn`).
- **Hyperparameter Tuning**: Used `GridSearchCV` to optimize model performance.

### Model Evaluation
- **Metrics**:
  - Mean Absolute Error (MAE)
  - Mean Squared Error (MSE)
  - R-squared (R²)
- **Analysis Tools**:
  - Residual analysis
  - Scatter plots for performance insights

---

## Visualizations
1. **Cost vs. Duration by Task Type**: A scatter plot highlighting the relationship between task duration and cost, segmented by task type.
2. **Feature Importance**: A bar plot displaying the contribution of each feature to the prediction model, identifying critical cost drivers.

---

## Tool Deployment
The tool was deployed using **Streamlit**, providing a user-friendly interface for cost predictions.

### Example Usage
1. Upload a CSV file with the following columns: `Task Type`, `Resources`, `Duration`.
2. The tool preprocesses the data, applies the trained model, and outputs predicted costs.

---

## Key Results
- Achieved a **Mean Absolute Error (MAE)** of ~500 USD on test data.
- Identified critical features influencing costs, such as `Duration` and `Task Type`.

---

## Future Enhancements
- **Real-World Data Integration**: Incorporate real-world pharmaceutical project data to improve prediction accuracy.
- **Advanced ML Models**: Support additional ML algorithms, such as XGBoost or deep learning frameworks.
- **Multi-Language Support**: Enable multi-language capabilities in the prediction tool interface.

---
