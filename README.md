# PRCP-1009 Cellphone Price Prediction

This project analyzes mobile phone specifications and builds a machine learning model to predict the **price range** of a mobile device using technical features such as battery power, RAM, internal memory, display resolution, connectivity options, and other hardware specifications.

## Project tasks covered

### Task 1: Data analysis report
The notebook includes a complete exploratory data analysis workflow:
- Dataset shape, data types, missing-value check, and duplicate-row check
- Descriptive statistics for all numeric columns
- Target class distribution analysis
- Correlation heatmap
- Distribution plots for important numerical features

### Task 2: Price range prediction
The notebook trains and compares multiple machine learning models to predict the target variable `price_range`.

Models evaluated:
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Random Forest
- Extra Trees
- Gradient Boosting
- Support Vector Classifier (SVC)

Evaluation methods used:
- Train-test split
- 5-fold stratified cross-validation
- Accuracy score
- Weighted F1-score
- Classification report
- Confusion matrix

### Task 3: Business impact and feature importance
The notebook explains how the final model helps business growth by:
- Identifying the most influential mobile specifications
- Supporting pricing strategy for new products
- Helping segment phones into low, medium, high, and premium price bands
- Reducing the risk of underpricing or overpricing devices
- Assisting product planning and specification optimization

## Files in the project

- `PRCP-1009-CellphonePrice.ipynb` — final Jupyter notebook submission
- `datasets_11167_15520_train.csv` — training dataset
- `model_comparison.csv` — performance comparison of all tested models
- `feature_importance.csv` — ranked feature importance values
- `analysis_summary.json` — compact project summary
- Chart files for target distribution, confusion matrix, correlation heatmap, and feature importance

## Dataset details

Target column:
- `price_range`
  - 0 = low cost
  - 1 = medium cost
  - 2 = high cost
  - 3 = very high cost

Some important input features:
- `battery_power`
- `blue`
- `three_g`
- `wifi`
- `ram`
- `int_memory`
- `px_height`
- `px_width`
- `mobile_wt`
- `talk_time`

## Workflow used

1. Load and inspect the dataset
2. Perform data quality checks
3. Conduct exploratory data analysis
4. Split features and target
5. Train multiple ML models
6. Compare models using validation metrics
7. Select the best-performing model
8. Interpret feature importance
9. Explain business value of the model

## Best model

In the generated version of the notebook, **Logistic Regression** achieved the best overall performance on this dataset based on test accuracy and cross-validation comparison.

## How to run

1. Open the notebook in Jupyter Notebook or JupyterLab.
2. Make sure the dataset CSV file is in the same folder as the notebook.
3. Install required libraries if needed:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

4. Run all cells from top to bottom.

## Notes

- If a column-selection error appears, print `df.columns.tolist()` and verify the exact column names.
- If needed, clean column names using:

```python
df.columns = df.columns.str.strip()
```

- The project is built as a multiclass classification problem, not a regression problem.

## Outcome

This project demonstrates how data analysis and machine learning can be used to estimate a mobile phone's market price segment from specifications alone. It also shows how model interpretation can support better product design, pricing decisions, and business expansion.
