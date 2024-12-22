# Bay Area Traffic Prediction Project 🚦

This project focuses on traffic flow prediction across the Bay Area's expressways, using statistical and machine learning techniques. The project employs R for data analysis, preprocessing, and modeling.

---

## 📌 **Objective**
To predict hourly traffic flow (Avg_Total_Flow) across Bay Area freeways and identify key factors influencing traffic congestion.

---

## 📂 **Project Structure**
- `data/`: Processed and summarized dataset.
- `scripts/`: R scripts for preprocessing, EDA, and modeling.
- `visuals/`: Power BI visualizations used in the project.
- `report/`: Final project report in `.pdf`.

---

## 🔍 **Key Features**
- **Preprocessing:** Handled missing data (~29%) and reduced dataset size (~15M rows to ~250k rows).
- **Feature Engineering:** Added derived features like `Lane Count`, `Weekend Flag`, and `Peak Hour Flag`.
- **Modeling:** Explored statistical and ML models, including:
  - Linear Regression
  - Decision Trees
  - XGBoost
  - Ridge and Lasso Regression

---

## 📈 **Performance**
| Model              | RMSE     | R-Squared | MAE     |
|---------------------|----------|-----------|---------|
| Linear Regression   | 629.14   | 0.8941    | 464.20  |
| Decision Tree       | 653.01   | 0.8859    | 506.11  |
| XGBoost             | 427.55   | 0.9515    | 303.03  |
| Ridge Regression    | 658.99   | 0.8851    | 498.15  |
| Lasso Regression    | 629.20   | 0.8940    | 463.80  |

---

## 🚀 **Future Scope**
- Hyperparameter tuning to enhance prediction accuracy.
- Incorporating additional data sources like:
  - Weather data
  - Incident data (accidents, lane closures)
  - FasTrak lane availability
- Time-series modeling for longer-term traffic trends.

---

## 🛠️ **Setup and Requirements**
- Install R and required libraries (`dplyr`, `caret`, `xgboost`, `glmnet`, etc.).
- Clone the repository:
  ```bash
  git clone https://github.com/your-username/Bay_Area_Traffic_Prediction.git
