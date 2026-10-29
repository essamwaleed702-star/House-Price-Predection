
# House Price Prediction

A machine learning project that explores a house-price dataset and
trains regression models to predict property sale prices.

## Project Overview

The goal of this project is to practice an end-to-end regression
workflow: exploring data, visualizing relationships, preparing features,
splitting the data, training models, and evaluating predictions.

## Technologies

-   Python
-   Pandas
-   Matplotlib
-   Seaborn
-   scikit-learn
-   Jupyter Notebook

## Dataset

The notebook loads the dataset from an Excel file named
`HousePricePrediction.xlsx`:

``` python
dataset = pd.read_excel("HousePricePrediction.xlsx")
```

Place that file in the same directory as the notebook before running it.
The dataset file is not included in this repository unless you add it
yourself. Make sure you have permission to redistribute it before
publishing it.

## Workflow

1.  **Load the data** from the Excel file using Pandas.
2.  **Explore the dataset** by inspecting its shape, data types, and
    categorical variables.
3.  **Visualize relationships** with a correlation heatmap and plots
    showing categorical-feature distributions.
4.  **Prepare the data** by dropping the `Id` column, handling missing
    values, and encoding categorical features with `OneHotEncoder`.
5.  **Split the data** into training and validation sets using an 80/20
    split and `random_state=0`.
6.  **Train regression models**:
    -   Linear Regression
    -   Random Forest Regressor
    -   Support Vector Regression (SVR)
7.  **Evaluate predictions** using Mean Absolute Percentage Error
    (MAPE).

## Project Structure

``` text
House-Price-Prediction/
├── House_Price_Prediction.ipynb
├── HousePricePrediction.xlsx   # Add the dataset file here
├── README.md


## Installation

Create and activate a virtual environment if desired, then install the
required packages:

``` bash
python -m venv .venv
```

On Windows:

``` bash
.venv\Scripts\activate
```

Install dependencies:

``` bash
pip install pandas matplotlib seaborn scikit-learn openpyxl jupyter
```

## Run the Notebook

1.  Clone or download this repository.
2.  Put `HousePricePrediction.xlsx` in the project directory.
3.  Install the dependencies listed above.
4.  Start Jupyter Notebook:

``` bash
jupyter notebook
```

5.  Open `House_Price_Prediction.ipynb` and run the cells from top to
    bottom.

## Models

  -----------------------------------------------------------------------
  Model                               Purpose
  ----------------------------------- -----------------------------------
  Linear Regression                   Baseline linear regression model

  Random Forest Regressor             Ensemble of decision trees for
                                      regression

  Support Vector Regression (SVR)     Regression model based on support
                                      vectors
  -----------------------------------------------------------------------

The notebook calculates MAPE for each model. Add the actual measured
results here after running the notebook; model performance is not stated
in this README because results can depend on the dataset and
environment.

## Possible Improvements

-   Split the data before fitting encoders, or use a scikit-learn
    `Pipeline` and `ColumnTransformer`, to avoid data leakage.
-   Do not fill missing target values (`SalePrice`) with the mean;
    consider removing rows where the target is missing.
-   Scale numerical features for SVR using `StandardScaler` inside a
    pipeline.
-   Compare models using MAE, RMSE, and R² in addition to MAPE.
-   Set `random_state` for reproducible Random Forest results and tune
    model hyperparameters.
-   Add an actual-versus-predicted plot and a model-comparison chart.
-   Save the trained model and optionally expose predictions through a
    small API.

## Current Limitations

-   The notebook expects a local Excel dataset file.
-   The notebook uses one train/validation split rather than
    cross-validation.
-   The current preprocessing fits `OneHotEncoder` before the
    train/validation split; this should be changed to a pipeline to
    avoid data leakage.
-   No performance values are included here because they should be
    copied from a fresh, verified notebook run.

## Author

**Essam Waleed**

www.linkedin.com/in/essam-waleed-9b2188421


## License

not license .
