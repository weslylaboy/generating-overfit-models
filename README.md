# Generating Overfit Models

This project explores the behavior of Decision Tree models as they increase in complexity. By default, scikit-learn's `DecisionTreeClassifier` continues to grow until every node is pure, which often leads to overfitting. This project investigates how the `max_depth` parameter affects model performance on training versus test data and aims to identify the point where overfitting begins.

## Objective

- Build multiple Decision Tree models with varying `max_depth` values.
- Track accuracy on both training and test datasets.
- Generate visualizations to analyze the relationship between tree depth and accuracy.
- Repeat the process with different data splits to confirm findings.
- Discuss the consequences of overfitting and its impact on building robust Decision Trees.

## Dataset

The project uses a small health dataset (`data/Whickham.txt`) containing information on individuals. The goal is to predict whether an individual survives (`outcome`) based on:
- `age`: Age of the individual.
- `smoker`: Whether the individual is a smoker (Yes/No).

## Methodology

1.  **Data Preparation**: Load the Whickham dataset and prepare features (`X`) and target (`y`).
2.  **Model Iteration**: For depths starting from `max_depth = 1` until the tree is fully grown, train a `DecisionTreeClassifier`.
3.  **Performance Tracking**: Record accuracy scores for both training and test sets at each depth.
4.  **Visualization**: Plot accuracies on the vertical axis against `max_depth` on the horizontal axis.
5.  **Overfitting Analysis**: Identify the depth where test accuracy begins to diverge significantly or decrease while training accuracy continues to improve.
6.  **Validation**: Repeat with different train/test splits to ensure results are consistent.

## Usage

To run the analysis, open the `overfit_models.ipynb` Jupyter Notebook and execute the cells.
