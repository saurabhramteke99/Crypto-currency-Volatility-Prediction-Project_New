# High-Level Design (HLD) Document

## Project Overview
Crypto Currency Volatility Prediction aims to forecast the volatility of various cryptocurrencies using historical market data and machine learning techniques.

## System Architecture
- **Data Source:** CSV file containing historical crypto data.
- **Preprocessing:** Data cleaning, encoding, scaling, feature engineering.
- **Modeling:** Random Forest Regressor with hyperparameter tuning.
- **Evaluation:** Metrics (MSE, RMSE, R²), visualizations.
- **Reporting:** Jupyter notebooks and markdown documentation.

## Major Components
- Data Ingestion
- Data Preprocessing
- Feature Engineering
- Model Training & Tuning
- Evaluation & Visualization

## Technologies Used
- Python, pandas, numpy, scikit-learn, matplotlib, seaborn, Jupyter Notebook

---

# Low-Level Design (LLD) Document

## Data Ingestion
- Read `dataset.csv` using pandas.
- Initial data inspection (`df.head()`, `df.dtypes`).

## Data Preprocessing
- Drop unnecessary columns (`Unnamed: 0`).
- Encode categorical features (`crypto_name` using LabelEncoder).
- Scale numerical features (MinMaxScaler or StandardScaler).

## Feature Engineering
- Create features: `daily_return`, `volatility`, `liquidity_ratio`, lagged and moving average features.
- Convert date columns to datetime.
- Extract time-based features: year, month, day, weekday, hour.

## Model Training & Tuning
- Split data into train/test sets.
- Train Random Forest Regressor.
- Hyperparameter tuning using RandomizedSearchCV.
- Tried so many models for training and this is what is best i go so far .

## Evaluation & Visualization
- Calculate metrics: MSE, RMSE, R².
- Visualize: Actual vs Predicted, Feature Importance, Volatility Distribution, Volatility Over Time, Correlation Heatmap.

## File Structure
- `EDA_Report.ipynb`: Main notebook for EDA, feature engineering, modeling, and visualization.
- `sourcecode.md`: Documentation of source code files.

## Functions/Classes
- Data loading and preprocessing functions.
- Feature engineering functions.
- Model training and evaluation functions.

---

