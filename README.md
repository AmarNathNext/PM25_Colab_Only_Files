# PM2.5 Air Quality Analysis and Regression

## Project Overview

This project explores air quality data and applies machine learning regression techniques to predict PM2.5 concentrations using meteorological and atmospheric variables.

The project focuses on data preprocessing, exploratory data analysis, regression modelling, and performance comparison.

## Dataset

The project uses an air quality dataset containing hourly observations from 2018.

- **Target variable:** PM2.5
- **Number of observations:** 8,116
- **Total columns:** 18
- **Time period:** January 2018 – December 2018

### Features

The dataset includes:

- PM2.5 concentration
- Temperature (T2M)
- Dew point temperature (T2MDEW)
- Surface pressure (PS)
- Total column water vapour (TQV)
- Total column cloud liquid water (TQL)
- Atmospheric and wind-related variables

The dataset contains missing values in some predictor variables, which are addressed during preprocessing.

## Project Workflow

1. Load the dataset and inspect its structure.
2. Convert and process date information.
3. Analyse missing values and data quality.
4. Perform exploratory data analysis.
5. Examine PM2.5 distributions and monthly patterns.
6. Apply missing-value imputation.
7. Prepare training and testing datasets.
8. Train regression models.
9. Evaluate and compare model performance.

## Machine Learning Models

The notebook implements and compares the following regression approaches:

- Linear Regression
- Decision Tree Regression
- Random Forest Regression
- Voting Regressor

## Model Evaluation

The models are evaluated using Root Mean Squared Error (RMSE).

| Model | Training RMSE | Testing RMSE |
|---|---:|---:|
| Linear Regression | 25.5 | 25.9 |
| Decision Tree | 0.0 | 28.8 |
| Random Forest | 7.2 | 20.1 |
| Voting Regressor | 10.5 | 21.8 |

The Random Forest model achieved the lowest test RMSE among the reported models.

The Decision Tree achieved zero training error but a higher test error, indicating overfitting.

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Repository Structure

```text
PM25_Colab_Only_Files/
│
├── Air_quality.ipynb
├── air_quality.csv
└── README.md
```

## How to Run

1. Clone this repository.
2. Install the required Python libraries.
3. Open `Air_quality.ipynb` using Jupyter Notebook or VS Code.
4. Ensure `air_quality.csv` is in the same directory.
5. Run the notebook cells sequentially.

Install the main dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

## Limitations and Future Improvements

- Evaluate the models using chronological train-test splitting to better reflect time-series prediction.
- Perform additional hyperparameter optimisation.
- Investigate feature importance and model interpretability.
- Evaluate additional metrics such as MAE and R².
- Document the original dataset source and variable units.

## Project Note

This project is an academic machine learning study focused on understanding the relationship between atmospheric variables and PM2.5 concentrations.

Dataset provenance and variable units should be verified against the original data source before publication or formal submission.
