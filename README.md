# California Housing Price Prediction

## Project Overview
This project predicts median house prices in California districts using the California Housing dataset. Three regression models were implemented and compared:

- **Linear Regression:** Assumes a linear relationship between features and house prices.  
- **Decision Tree Regressor:** Captures non-linear patterns by splitting data based on feature values.  
- **Random Forest Regressor:** An ensemble of decision trees that improves accuracy and reduces overfitting.

The dataset includes features such as median income, house age, number of rooms, population, and location coordinates. The target variable is the median house value (**MedHouseVal**).

---

## Dataset
**Source:** `sklearn.datasets.fetch_california_housing`

**Features:**
- `MedInc` – Median income of households  
- `HouseAge` – Average age of houses  
- `AveRooms` – Average number of rooms per household  
- `AveBedrms` – Average number of bedrooms per household  
- `Population` – District population  
- `AveOccup` – Average occupancy per household  
- `Latitude` & `Longitude` – Location coordinates  

**Target:**  
- `MedHouseVal` – Median house value for the district  

---

## Data Preprocessing
- Checked for missing values and duplicates (none found).  
- Handled outliers using capping to reduce extreme values.  
- Scaled features using `StandardScaler` for normalization.  
- Split data into **training (80%)** and **testing (20%)** sets.

---

## Regression Models Implemented
- **Linear Regression:** Simple baseline for predicting house prices.  
- **Decision Tree Regressor:** Splits the data to capture non-linear relationships.  
- **Random Forest Regressor:** Combines multiple decision trees to improve accuracy and generalization.

---

## Evaluation Metrics
- **Mean Squared Error (MSE):** Measures average squared prediction errors.  
- **Mean Absolute Error (MAE):** Measures average absolute prediction errors.  
- **R2 Score:** Shows the proportion of variance explained by the model.

---

## Key Observations
- **Random Forest Regressor** performed best with the lowest errors and highest R², capturing complex relationships while avoiding overfitting.  
- **Decision Tree Regressor** performed the worst due to overfitting.  
- **Linear Regression** provided a reasonable baseline but could not fully capture non-linear patterns.

---

## Conclusion
- **Recommended Model:** Random Forest Regressor for accurate house price prediction.  
- **Linear Regression:** Useful for understanding feature impacts but less accurate.  
- **Decision Trees:** Alone, they may overfit; ensemble methods like Random Forest are preferred.

