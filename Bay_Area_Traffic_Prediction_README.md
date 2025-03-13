
# Bay Area Traffic Prediction

## 🚗 Project Overview
This project aims to predict hourly traffic flow across Bay Area expressways (US-101, I-80, I-280, I-880) using statistical and machine learning techniques. By analyzing historical traffic data, we developed predictive models to support urban planning, optimize traffic management, and improve road safety.

## 📚 Data Description
- **Source:** Caltrans PeMS (Performance Measurement System) – District 4 (Bay Area)
- **Data Size:** ~15 million records processed into ~250k for modeling
- **Key Features:**
  - **Time Variables:** Hour, Day Name (Weekday/Weekend), Peak Hour Flags
  - **Traffic Metrics:** Average Total Occupancy, Average Speed, Number of Lanes
  - **Route Information:** Identified based on expressway segments

## 🔄 Data Preprocessing
- **Handled Missing Values:** Addressed ~29% missing data using imputation and removal strategies.
- **Feature Engineering:**
  - Created binary flags for **Peak Hours** and **Weekends**.
  - Extracted **Day Type**, **Route**, and **Lane Count** metrics.
  - Normalized numeric variables to standardize data for modeling.

## 🔍 Exploratory Data Analysis (EDA)
- Conducted analysis in **Power BI** and **R** to:
  - Identify traffic trends by day and hour.
  - Analyze correlations between variables like speed, occupancy, and lane counts.
  - Visualize missing data patterns and handle outliers.

## 🧠 Modeling Approach
Applied various regression models to forecast hourly traffic flow:
1. **Linear Regression** – Baseline model for interpretability.
2. **Decision Tree** – Captured non-linear relationships.
3. **Ridge & Lasso Regression** – Regularization to prevent overfitting.
4. **XGBoost** – Advanced model achieving the best performance.

### 🎯 Model Evaluation Metrics:
- **R² Score** (Explained Variance)
- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Error (MAE)**

| Model               | R²    | RMSE  | MAE   |
|---------------------|-------|-------|-------|
| Linear Regression   | 0.894 | 629.1 | 464.2 |
| Decision Tree       | 0.886 | 653.0 | 506.1 |
| Ridge Regression    | 0.885 | 658.9 | 498.1 |
| Lasso Regression    | 0.894 | 629.2 | 463.8 |
| **XGBoost (Best)**  | **0.951** | **427.5** | **303.0** |

## ✅ Key Findings & Insights
- **XGBoost** achieved the highest accuracy with an R² of **0.95**.
- Top predictors for traffic flow include:
  - **Avg_Total_Occupancy** – Reflects congestion density.
  - **Avg_Lanes_Count** – More lanes typically lead to higher flow rates.
  - **Avg_Speed** – Lower speeds during peak congestion periods.
  - **Peak_Hour_Flag** – Higher traffic flow during rush hours.
  - **Route** – Distinct traffic patterns based on the route.

## 📊 Visualizations
- Line plots of hourly traffic flow trends.
- Correlation heatmaps showcasing variable relationships.
- Actual vs. Predicted traffic flow comparisons.

## 🚀 How to Run the Project
1. **Prerequisites:**
   - Install R and required packages: `dplyr`, `ggplot2`, `xgboost`, `caret`.
2. **Execution Steps:**
   - Clone the repository.
   - Navigate to the scripts folder and run the `traffic_prediction.R` script.
   - Use the provided datasets in the `data/` folder.
3. **Output:**
   - Model performance metrics and visualizations.

## 🔮 Future Work
- Integrate **real-time data** for dynamic predictions.
- Include external factors like **weather and accident data**.
- Explore deep learning models (e.g., LSTM for time-series forecasting).

## 💡 Business Impact
- Enables urban planners to optimize traffic signals and manage congestion effectively.
- Supports real-time traffic forecasting for intelligent transportation systems.
- Enhances public safety by predicting and managing traffic spikes.

## 📄 License
This project is licensed under the [MIT License](LICENSE).

## 🙌 Acknowledgements
- Thanks to **Caltrans PeMS** for the dataset.
- Special recognition to the academic teams guiding the project methodology.

---
Feel free to fork, star, or contribute to this repository if you find it useful!
