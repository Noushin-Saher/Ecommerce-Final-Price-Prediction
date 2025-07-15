# E-Commerce Final Price Prediction

## 📌 Project Description
This project aims to predict the final price of products in an e-commerce setting using machine learning techniques. It uses product-related features like brand, category, color, size, reviews, and initial price to estimate final discounted prices for optimizing pricing strategies.

## 📊 Dataset
- **Name:** Shein-dataset-samples  
- **Source:** [GitHub Dataset](https://github.com/luminati-io/Shein-dataset-samples/blob/main/shein-products.csv)  
- **Samples:** 1001  
- **Features used:** color, size, category, brand, initial_price, reviews_count, rating, in_stock  
- **Target Variable:** `final_price`

## 🧪 Objective
- Predict the final price using selected features  
- Compare Linear Regression and Random Forest Regressor  
- Evaluate different train-test splits (70:30, 75:25, 80:20)  
- Finalize the best-performing model and configuration  

## 🛠️ Tools & Libraries
- **Language:** Python  
- **Libraries:** pandas, numpy, scikit-learn (LinearRegression, RandomForestRegressor), LabelEncoder, matplotlib  

## 🧠 Algorithms Used
- **Linear Regression**  
- **Random Forest Regressor (Final Model)**

## ⚙️ Methodology
1. **Data Preprocessing**  
   - Handled missing values and removed duplicates  
   - Encoded categorical features (e.g., brand, category, color) using `LabelEncoder`  
2. **Feature Selection**  
   - Focused on features directly impacting price: `initial_price`, `rating`, `reviews_count`, `brand`, `category`, etc.  
3. **Model Comparison**  
   - Trained models on different splits (70:30, 75:25, 80:20)  
   - Evaluated using MAE, RMSE, and R² Score  
4. **Final Model**  
   - **Random Forest Regressor with 80:20 split**  
   - Delivered high R² Score (~0.98) and low MAE  

## 📈 Results

| Model                 | Split | MAE   | RMSE  | R² Score |
|----------------------|-------|-------|-------|----------|
| Linear Regression     | 80:20 | 6.34  | 13.73 | 0.98     |
| Random Forest Regressor | 80:20 | 7.78  | 45.54 | 0.79     |

> ✅ Final Model: **Random Forest Regressor** (best trade-off of generalization and accuracy)

## 🔍 Example Prediction
Given inputs like:
```json
{
  "color": "Black",
  "size": "220V-240V",
  "category": "Hot Plates",
  "brand": "SHEIN",
  "initial_price": 299.2,
  "reviews_count": 0,
  "rating": 0.0,
  "in_stock": "True"
}
