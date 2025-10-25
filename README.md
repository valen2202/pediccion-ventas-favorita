# Store Sales Time Series Forecasting

This project was created as a challenge inspired by the **Kaggle Competition: Store Sales - Time Series Forecasting**.  
The objective: **to predict the sales of a supermarket chain in Ecuador**, combining factors such as calendar data, holidays, oil prices, and time series seasonality.

---

## Motivation
Retail sales depend not only on natural demand but also on external variables such as holidays, promotions, and global events.  
This project aims to capture these patterns and build a robust model capable of forecasting sales with greater accuracy.

---

## Project Stages

1. **Data Loading and Preparation**  
   - Conversion of dates to `datetime`.  
   - Integration of datasets: holidays, oil prices, and sales.  

2. **Feature Engineering**  
   - Creation of calendar-based features (day, month, year, day of the week).  
   - Inclusion of holidays using dummy variables.  
   - Moving averages on oil prices to capture trends.  

3. **Exploratory Data Analysis (EDA)**  
   - Visualization of sales vs oil price.  
   - Analysis of seasonality and trends.  

4. **Modeling**  
   - **XGBoost** and **LightGBM** as main models.  
   - One-hot encoding applied to categorical variables (`family`).  

5. **Evaluation**  
   - Metrics: RMSE, MAPE, Adjusted R², and NWRMSLE (official Kaggle metric).  
   - Comparison between predicted and actual values.  

6. **Optimization**  
   - GridSearch for XGBoost hyperparameter tuning.  
   - Cross-validation for robustness.  

---

## Results
- The models successfully captured key seasonal patterns.  
- A meaningful correlation was observed between sales, oil prices, and seasonality.  
- LightGBM provided better training efficiency, while XGBoost showed competitive performance after tuning.  

---

## Conclusions
The project confirms that:  
- **Feature engineering** in time series (holidays, external prices, calendar variables) makes a significant difference.  
- Gradient boosting models (XGBoost/LightGBM) are particularly powerful in scenarios with multiple external variables.  

---

## Technologies Used
- Python, Pandas, NumPy  
- Matplotlib, Seaborn  
- XGBoost, LightGBM  
- Scikit-learn

