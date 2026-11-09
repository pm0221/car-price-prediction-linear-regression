# Car Price Prediction Using Linear Regression

## Project Overview
This project builds a **Linear Regression** model to predict car prices using numerical and encoded features from a car-price dataset. The analysis is performed in the Jupyter Notebook `linear_regression_da.ipynb`.

The notebook loads `CarPrice.csv`, explores the dataset, prepares the input features, trains a Linear Regression model, and evaluates its predictions.

## Objectives
- Explore and understand the car-price dataset.
- Select relevant input features and the target variable.
- Clean and transform selected categorical values.
- Convert categorical features into numerical dummy variables.
- Scale the feature data.
- Train a Linear Regression model.
- Evaluate model performance using Mean Squared Error and R-squared.

## Dataset
The notebook expects a CSV file named **`CarPrice.csv`** in the working directory.

- **Target variable:** `price`
- **Excluded column:** `car_ID`
- **Input features:** Numerical car attributes, together with encoded categorical attributes.

Make sure `CarPrice.csv` is available in the same folder as the notebook before running it. The notebook does not download the dataset automatically.

## Workflow

### 1. Import Libraries
The notebook uses Pandas, Seaborn, Matplotlib, and Scikit-learn for data handling, visualization, preprocessing, model training, and evaluation.

### 2. Load and Explore the Data
- Read `CarPrice.csv` into a Pandas DataFrame.
- Display the first rows of the dataset.
- Separate `price` as the target (`Y`).
- Remove `price` and `car_ID` from the predictors.
- Select numerical columns for the initial feature exploration.
- Check missing values and view descriptive statistics.

### 3. Data Visualization
The notebook uses pair plots, scatter-matrix plots, a distribution plot of car prices, and a plot of the target values to explore patterns in the data.

### 4. Data Preprocessing
- Convert `doornumber` values such as `four` and `two` into numeric values.
- Convert written `cylindernumber` values into numbers.
- Extract the first word from `CarName` as the manufacturer name.
- Standardize several manufacturer-name spelling variants.
- Apply one-hot encoding with `pandas.get_dummies()` to categorical columns.

### 5. Feature Scaling
Scale the prepared feature matrix using Scikit-learn's `scale()` function.

### 6. Train-Test Split
Split the data into training and testing sets:
- Test size: **30%**
- Random state: **42**

### 7. Model Training
Train a Scikit-learn `LinearRegression` model using the training data.

### 8. Model Evaluation
Predict car prices for the test data and calculate:
- **Mean Squared Error (MSE):** Measures the average squared prediction error.
- **R-squared (R²):** Indicates the proportion of target variance explained by the model.

The notebook also prints the learned regression coefficients.

## Technologies and Libraries
- Python
- Pandas
- NumPy (available as a common numerical dependency; not explicitly imported in the notebook)
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Installation

Install the required packages:

```bash
pip install pandas matplotlib seaborn scikit-learn jupyter
```

## How to Run
1. Keep `linear_regression_da.ipynb` and `CarPrice.csv` in the same project folder.
2. Open a terminal in that folder.
3. Start Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

4. Open `linear_regression_da.ipynb`.
5. Run the notebook cells in order.

## Project Structure

```text
.
├── linear_regression_da.ipynb
├── CarPrice.csv
└── README.md
```

## Evaluation Metrics
| Metric | Purpose |
|---|---|
| Mean Squared Error (MSE) | Measures the average squared difference between actual and predicted prices. Lower is better. |
| R-squared (R²) | Measures how much variation in car prices is explained by the model. |

## Notes
- The dataset file `CarPrice.csv` is required and is not included automatically by the notebook.
- The notebook scales the feature matrix before fitting the model.
- Numerical results depend on the contents of the dataset and the execution environment.
- The notebook reports MSE, R², and model coefficients when executed.

## Author
Add your name and academic details here.
