# JORDAN
# 👟 Air Jordan Resale Price Prediction

## Problem Statement
Predict the resale price of Air Jordan sneakers based on 
shoe model, colorway, condition, and retail price. Useful 
for resellers and platforms like StockX and GOAT to 
estimate market value.

## Dataset
- **Source:** Kaggle Datasets
- **Features:** Shoe model, colorway, condition, retail price, 
  sales channel, profit margin, days in inventory
- **Target:** Resale_Price_USD

## Approach
- Detailed EDA including profit margin analysis by shoe model 
  and sales channel performance comparison
- Ordinal encoding for Condition (Deadstock → VNDS → Used)
- One-hot encoding for Shoe_Model
- Feature scaling using StandardScaler
- GridSearchCV hyperparameter tuning for Lasso and Ridge
- Feature importance extracted from RandomForest

## Results
| Model | R² | RMSE |
|---|---|---|
| Linear Regression | ~0.713 | ~84 |
| Lasso Regression | ~0.714 | ~84 |
| Ridge Regression | ~0.713 | ~84 |
| **Random Forest** | **0.728** | **83.91** |

## Key Findings
- Random Forest performed best but improvement over linear 
  models was modest — suggesting a mostly linear relationship 
  between features and resale price
- GOAT and StockX are the most efficient sales channels 
  with the lowest days in inventory
- Retail price and shoe model are the strongest predictors 
  of resale value

## Libraries Used
Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
