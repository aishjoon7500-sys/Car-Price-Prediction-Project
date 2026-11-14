# Car Price Prediction Using Linear Regression

## Project Overview

This project uses Python and machine learning to estimate the selling
price of a used car based on its characteristics. It explores a used-car
dataset, performs exploratory data analysis (EDA), prepares the data for
modelling, and trains a **Linear Regression** model to predict selling
prices.

The objective is to understand how factors such as a car's manufacturing
year, kilometres driven, fuel type, transmission, engine capacity,
mileage, and ownership history relate to its selling price.

## Dataset

The notebook works with a dataset containing **7,907 records and 12
columns** at the initial inspection stage.

  Column                 Description
  ---------------------- -----------------------------------
  `Car_Name`             Name/model of the car
  `Year`                 Manufacturing year
  `Selling_Price`        Selling price (prediction target)
  `KM_Driven`            Kilometres driven
  `Fuel`                 Fuel type
  `Seller_Type`          Type of seller
  `Transmission`         Transmission type
  `Owner`                Ownership category
  `Mileage(km/ltr/kg)`   Mileage
  `Engine`               Engine capacity
  `Max_power`            Maximum power
  `Seats`                Number of seats

The notebook reports one missing value in `Max_power` during the initial
data-quality check. The modelling target contains **7,906 records**.

> **Dataset file:** The Excel dataset is referenced through a local
> Windows file path in the notebook and is not embedded in the notebook.
> Place the dataset in your project folder or update the file path in
> the data-loading cell before running the notebook.

## Tools & Libraries

-   **Python** -- programming language
-   **Pandas** -- data loading and manipulation
-   **NumPy** -- numerical operations
-   **Matplotlib** -- data visualization
-   **Seaborn** -- statistical plots
-   **Scikit-learn** -- train-test split, Linear Regression, and model
    evaluation
-   **Jupyter Notebook** -- development environment

## Project Workflow

### 1. Data Loading and Inspection

-   Imported the Excel dataset using Pandas.
-   Checked the dataset dimensions, columns, sample records, and data
    types.
-   Reviewed descriptive statistics and missing values.

### 2. Exploratory Data Analysis (EDA)

Used visualizations and frequency counts to explore: - Distribution of
manufacturing years, selling prices, and kilometres driven. -
Distribution of fuel types and seller types. - Selling price across
transmission types. - Relationship between selling price and mileage. -
Relationship between selling price and engine capacity.

### 3. Data Preparation

-   Converted categorical columns (`Car_Name`, `Fuel`, `Seller_Type`,
    `Transmission`, and `Owner`) into numeric category codes.
-   Separated the independent variables from the target variable,
    `Selling_Price`.

### 4. Model Building

-   Split the data into training and testing sets.
-   Used a **75:25 train-test split** with `random_state=0`.
-   Trained a Linear Regression model using Scikit-learn.

### 5. Model Evaluation

Evaluated model performance using: - Mean Squared Error (MSE) -
R-squared (R²) score

## Model Performance

  Evaluation Metric                            Result
  -------------------------- ------------------------
  R-squared (R²)                  **0.6782 (67.82%)**
  Mean Squared Error (MSE)     **214,920,480,253.30**

The model achieved an R² score of **67.82%**, indicating that it
explains approximately 67.82% of the variation in selling prices in the
test dataset.

This is a baseline Linear Regression result. Model performance may be
improved through further feature engineering, more appropriate
categorical encoding, outlier analysis, and comparison with other
regression algorithms.

## Repository Structure

``` text
Car-Price-Prediction/
│
├── Car_Price_Prediction_Project.ipynb
├── README.md
└── CarDekho_Dataset.xlsx   # Add locally if you have permission to share it
```

## Future Improvements

-   Apply more robust categorical encoding, such as one-hot encoding.
-   Investigate and handle missing values and outliers systematically.
-   Perform feature selection and feature engineering.
-   Compare Linear Regression with Random Forest, Decision Tree, and
    other regression models.
-   Evaluate additional metrics such as RMSE and MAE.
-   Tune model parameters and validate performance using
    cross-validation.

## Author

**Aish Joon**

M.Sc. Statistics \| Data Analytics \| Python \| SQL \| Power BI \|
Machine Learning

------------------------------------------------------------------------

*This project was developed as a practical exercise in exploratory data
analysis, data preparation, regression modelling, and model evaluation
using Python.*
