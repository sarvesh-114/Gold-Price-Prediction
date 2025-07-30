# 🪙 Gold Price Forecasting (1950–2020)

This project analyzes and forecasts monthly gold prices from 1950 to 2020 using classical time series models. The objective is to understand long-term trends, evaluate prediction models, and identify patterns in historical pricing data.

---

## 📂 Dataset Overview

- **Source:** Historical gold prices (CSV format)
- **Period Covered:** January 1950 – August 2020
- **Frequency:** Monthly
- **Columns:**
  - `Date`: In YYYY-MM format
  - `Price`: Monthly average gold price in USD

---

## 🧰 Technologies Used

- **Language:** Python
- **Libraries:**  
  - `pandas`, `numpy` for data handling  
  - `matplotlib`, `seaborn` for visualization  
  - `scikit-learn` for Linear Regression  
  - `statsmodels` for time series forecasting (`Holt`, `ExponentialSmoothing`)  

---

## 📊 Exploratory Data Analysis (EDA)

- Converted date column to proper datetime format and set it as the index.
- Visualized:
  - Overall price trends
  - Yearly and monthly seasonality via box plots
  - Rolling averages (yearly, quarterly, and decade-based)

---

## 🔍 Forecasting Models

Three forecasting models were implemented and compared:

### 1. **Naive Forecasting**
- Assumes future prices equal the last known price.
- **MAPE:** ~18%

### 2. **Linear Regression on Time**
- Models price as a linear function of time (numeric timeline).
- **MAPE:** ~30%

### 3. **Exponential Smoothing**
- Captures both **trend** and **seasonality**.
- **MAPE:** < 10%
- Provided best performance and was selected as the final model.

---

## 📈 Final Forecasting & Confidence Interval

- Forecast generated using `ExponentialSmoothing` model for the test set (2016–2020).
- 95% Confidence Intervals computed and visualized.
- Visualization includes:
  - Actual prices
  - Predicted values
  - Forecast range (upper and lower bounds)

---

## 🧪 Model Evaluation Metric

- **MAPE (Mean Absolute Percentage Error)** was used to compare the models:
  
| Model                | MAPE (%) |
|---------------------|----------|
| Linear Regression    | ~30%     |
| Naive Forecasting    | ~18%     |
| Exponential Smoothing | < 10%    |

---

## 📌 Key Learnings

- Understood how to prepare and analyze long-term time series data.
- Compared different forecasting techniques using a standard evaluation metric (MAPE).
- Gained hands-on experience in visualizing patterns, trend shifts, and seasonality in financial data.

---

## 📁 Files

| File | Description |
|------|-------------|
| `gold_monthly_csv.csv` | Dataset used for analysis |
| `gold_price_prediction.ipynb` | Complete analysis and model implementation notebook |
| `README.md` | Project documentation (this file) |

---

## 🧠 Future Improvements

- Implement ARIMA or Prophet models for comparison.
- Include external factors like inflation or stock market indices.
- Create a Streamlit app for interactive visualization.

---

## 👨‍💻 Author

**Sarvesh Jathar**  
_This project was built to gain practical understanding of time series forecasting and model evaluation._

---

## 📜 License

This project is for educational purposes and is open-source. Attribution appreciated.

