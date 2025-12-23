# 🏠 House Price Prediction

Predict house prices based on property features using **Linear Regression**.


**Overview**

This project predicts house prices (in lakhs) using features like area, bedrooms, bathrooms, stories, and amenities. It includes preprocessing, scaling, log transformation, and model evaluation.


## **Dataset**

* **545 houses** with features such as area, bedrooms, bathrooms, stories, mainroad, guestroom, basement, hotwaterheating, airconditioning, parking, prefarea, furnishingstatus
* Target: `price` (INR)



## **Preprocessing**

* Categorical to numeric conversion (`yes/no` → 1/0, furnishingstatus → 0/1/2)
* Outlier removal using **IQR method**
* Scaling numeric features (`area`, `bedrooms`, `bathrooms`, `stories`, `parking`)
* Optional log-transform on price to reduce skew



## **Model**

* **Linear Regression** (scikit-learn)
* Trained on scaled features
* Predicts house price for new input



## **Evaluation**

* **RMSE:** 0.22 lakhs (after log-transform)
* **R² Score:** 0.72

> Log transform improves interpretability and reduces the effect of extremely high prices.



## **Usage**

```python
import pandas as pd
import numpy as np
from sklearn.preprocessing import StandardScaler

# Example: Predict new house price
new_house = [[3000, 3, 3, 2, 1, 1, 1, 1, 2, 1, 2]]
new_df = pd.DataFrame(new_house, columns=X.columns)
new_df[numeric_features] = scaler.transform(new_df[numeric_features])
predicted_price = np.expm1(model.predict(new_df))
print(f'Predicted House Price: {predicted_price[0]:.2f} lakhs')
```


## **Visualizations**

* Scatter plots (feature vs price)
* Histogram of price distribution
* Boxplot for outlier detection


## **Future Improvements**

* Feature engineering (e.g., `total_rooms = bedrooms + bathrooms + stories`)
* Try tree-based models: Random Forest, XGBoost
* Hyperparameter tuning for Ridge/Lasso regression


## **Technologies**

* Python 3, Pandas, NumPy, Matplotlib
* scikit-learn (LinearRegression, StandardScaler, metrics)

