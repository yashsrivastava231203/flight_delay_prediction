# Flight Delay Prediction

This project is a supervised machine learning system that predicts whether a flight will be delayed by more than **60 minutes** before its scheduled departure.  
The model is built using **XGBoost**, which is highly effective for tabular data and captures nonlinear interactions without heavy manual feature engineering.

## 📌 Problem Statement
Flight delays can cause operational disruptions for airlines and significant inconvenience for passengers.  
By predicting significant delays ahead of time, airlines can take proactive measures such as reassigning crew, rebooking passengers, or adjusting schedules.

## 📊 Dataset & Features
The dataset includes:
- **Airline** — operating carrier
- **Departure Time** — scheduled departure time
- **Origin & Destination Airports**
- **Day of Week**
- **Date** (used to extract month and day)
- **Carrier Delay (minutes)** — actual recorded delay

## 🛠 Preprocessing
- Converted `Date` to `month` and `day` features.
- Created binary target: `is_delayed_60+` (1 if carrier delay > 60 min, else 0).
- Encoded categorical features using Label Encoding.

## 🤖 Model
- **Algorithm:** XGBoost Classifier (`eval_metric='logloss'`)
- **Why XGBoost?** Handles mixed data types, captures nonlinearities, and provides regularization to reduce overfitting.
- **Train/Test Split:** 70/30

## 📈 Evaluation
- **Metrics:** ROC-AUC, precision, recall, confusion matrix
- **ROC-AUC** used to measure threshold-independent model performance
- Balanced precision and recall to manage trade-offs between false positives and false negatives

## 🚀 Future Improvements
- Add weather and airport congestion data
- Use time-based validation for realistic deployment scenarios
- Apply SHAP values for interpretability

## ⚙️ Tech Stack
- Python
- Pandas, NumPy
- scikit-learn
- XGBoost
- Matplotlib / Seaborn (for visualizations)

---

**Author:** Yash Srivastava
