# British-airways-customer-booking-prediction

## Project Overview
This project focuses on applying machine learning to a customer booking dataset to predict whether a customer will complete a flight/holiday booking. The goal is to develop a proactive customer acquisition strategy by identifying the most influential factors (features) that drive booking completion.

## Methodology
1.  **Data Exploration & Cleaning:** Handled missing values, standardized column names, and dropped duplicates.
2.  **Feature Engineering:** Created new features such as `booking_region`, `num_extra_services`, and a binned ratio of `purchase_lead` to `length_of_stay` to enhance predictive power.
3.  **Modeling:** Trained a **Random Forest Classifier** to ensure interpretability (feature importance). The target variable is `booking_complete`.
4.  **Evaluation:** Conducted 5-fold cross-validation and assessed performance using the **ROC AUC** score.

## Key Findings & Model Performance
* **Model Performance:** The Random Forest achieved an **ROC AUC of approximately 0.72**, indicating a decent ability to rank positive cases higher than negative ones.
* **Top Predictors (Feature Importance):**
    1.  **`purchase_lead`**: Shorter lead times correlate highly with completion.
    2.  **`flight_duration` / `length_of_stay`**: Indicators of a higher-commitment trip.
    3.  **`num_extra_services`**: Customers requesting more services (baggage, meals) are more likely to commit.

## Files in this Repository
* `customer_booking.csv`: The raw dataset.
* `notebook.ipynb`: The Jupyter Notebook containing all the analysis code.
