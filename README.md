# Bank-Customer-Churn-Data-Analysis

This project aims to predict customer churn for a bank by analyzing and modeling customer data. Using exploratory data analysis, feature engineering, and the Gradient Boosting Classifier, this analysis identifies key churn drivers and provides insights into customer behavior.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Data Description](#data-description)
3. [Installation and Requirements](#installation-and-requirements)
4. [Project Structure](#project-structure)
5. [Usage](#usage)
6. [Results](#results)
7. [Contributing](#contributing)

---

## Project Overview

The project uses historical customer data to model and predict churn, defined as customers who stop using the bank's services. The project applies machine learning models, specifically **Gradient Boosting Classifier**, and performs **grid search** for hyperparameter tuning. It is implemented in Python with exploratory data analysis (EDA), feature engineering, model training, and evaluation stages.

## Data Description

The dataset includes two files:
- `bankChurn.csv`: Main dataset containing customer details and churn status.
- `externalData.csv`: Additional customer attributes.

The target variable is `CHURN_CUST_IND`, where:
- 1 indicates a customer who has churned.
- 0 indicates a customer who has not churned.

### Key Features in the Dataset:
- **Demographic Information**: Age, gender, etc.
- **Account Details**: Account balance, transaction history, loan information, etc.
- **Transaction Behavior**: Transaction counts, average transaction amounts, and more.

## Installation and Requirements

### Prerequisites

Ensure you have Python installed (version 3.6 or higher). You will need the following libraries:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `statsmodels`
- `scipy`
- `scikit-learn`

### Install the Requirements

```bash
pip install -r requirements.txt
```

> **Note**: Replace `requirements.txt` with the list of required packages if you haven't created this file.

## Project Structure

The project is structured into multiple sections:

1. **Data Loading**: Loads the `bankChurn.csv` and `externalData.csv` datasets and explores their structure and summary statistics.
2. **Exploratory Data Analysis (EDA)**: Visualizes distributions, correlations, and patterns in the data.
3. **Feature Engineering**: Derives additional features for improved model performance.
4. **Data Preprocessing**: Handles missing values, encodes categorical variables, and standardizes numerical data.
5. **Modeling**: Builds and evaluates a Gradient Boosting Classifier, with hyperparameter tuning via Grid Search.

### Files and Folders
- `bankChurn.csv` and `externalData.csv`: Data files.
- `modelData.csv`: Processed dataset ready for modeling.
- `notebook.ipynb`: Jupyter notebook containing the analysis.
- `README.md`: Project documentation.

## Usage

1. **Run the Jupyter Notebook**:
   - Open `notebook.ipynb` in Jupyter Notebook or JupyterLab.
   - Run each cell sequentially to load data, perform analysis, and build models.

2. **Execute in Python**:
   - If running from a script, ensure all dependencies are installed.
   - Load the notebook contents step by step in a Python IDE or environment.

### Key Code Functions

- **EDA**: `plot_distribution()` and `NumVarPerf()` for visualizing data distributions.
- **Feature Engineering**: `Encoder()` and `ColumnDivide()` for creating additional features.
- **Modeling**: `GradientBoostingClassifier()` for classification with grid search optimization.

## Results

The model achieves the following performance metrics:
- **Accuracy**: Provided on the test set as an output of the Gradient Boosting Classifier.
- **ROC-AUC**: Output from GridSearchCV optimization to select the best model configuration.

### Key Insights

- Customers with lower account balances are more likely to churn.
- Customers with missing home address information show a higher churn rate.

These insights provide actionable strategies for customer retention, focusing on high-risk groups.

## Contributing

Contributions are welcome! Feel free to submit a pull request or raise an issue if you have suggestions for improving the project.


---

### Contact

For questions or issues, please reach out via GitHub.
