# House-price-prediction-using-Linear-Regression-and-Random-Forest

# House Price Prediction

A beginner machine learning project that explores a house price dataset and compares **Linear Regression** with **Random Forest Regression**. Both models use `Area` to predict `Price`.

## Project files

- `project1_house_price_prediction.ipynb` — data exploration, visualizations, model training, and evaluation
- `House Price Prediction Dataset.csv` — dataset used by the notebook
- `house_price_model.pkl` — saved Random Forest model

## Dataset

The dataset contains house details including `Area`, `Bedrooms`, `Bathrooms`, `Floors`, `YearBuilt`, `Location`, `Condition`, `Garage`, and `Price`. `Id` identifies each row.

## What the notebook does

1. Loads the CSV file with pandas.
2. Displays sample rows, dimensions, column types, summary statistics, and missing-value counts.
3. Creates basic KPIs and exploratory plots:
   - Price distribution histogram
   - House count by location
   - Area versus price scatter plot
4. Splits the data into training and test sets (80% / 20%, `random_state=42`).
5. Trains Linear Regression and Random Forest Regression models using `Area` as the only input feature.
6. Evaluates both models with R², Mean Squared Error (MSE), and Mean Absolute Error (MAE).
7. Saves the Random Forest model as `house_price_model.pkl` using Joblib.

## Model results

The following values are transcribed from the notebook screenshots. They use the same train/test split and `Area` feature.

| Model | R² | MSE | MAE |
|---|---:|---:|---:|
| Linear Regression | -0.0007 | 77,856,127,383.18 | 242,478.32 |
| Random Forest Regressor | -0.4199 | 110,465,527,484.07 | 274,376.60 |

Both R² values are below zero on this test split, so these models performed worse than predicting the test-set average price. The results suggest that `Area` alone is not enough for reliable predictions in this dataset. Metrics can vary if the data or split changes.

## Requirements

- Python
- pandas
- NumPy
- Matplotlib
- scikit-learn
- Joblib
- Jupyter Notebook (to run the `.ipynb` file)

Install the Python packages with:

```bash
pip install pandas numpy matplotlib scikit-learn joblib jupyter
```

## Run the project

Place the notebook and CSV file in the same folder, then start Jupyter:

```bash
jupyter notebook
```

Open `project1_house_price_prediction.ipynb` and run the cells from top to bottom. The notebook expects the CSV filename to be:

```text
House Price Prediction Dataset.csv
```

The final Random Forest model is saved in the current working directory as `house_price_model.pkl`.

## 🛠️ Built With

Python · Pandas · NumPy · Matplotlib · scikit-learn · Joblib

---

## 👤 Author

**Mishkat**
Learning my way toward AI and Agentic Engineering, one project at a time.
