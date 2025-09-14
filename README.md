# Predicting-California-Housing-Prices

# 🏡 California Housing Price Prediction

## 📌 Project Overview
This project focuses on building a **predictive model** to estimate **Median House Value** using demographic and geographic features from the **California Housing Dataset**.  

The objective is to create a **robust and accurate model** that can assist in **investment decisions, pricing strategies, and policy planning**.

---

## 📊 Exploratory Data Analysis (EDA)

- **Dataset size:** ~20,000 rows  
- **Features:** Number of rooms, population, median income, geographic location  
- **Target:** Median House Value  

### 🔑 Key Insights
- **Median income** is the strongest predictor of house value.  
- Relationship between income and house value is **non-linear** → simple linear regression is insufficient.  
- Data preprocessing included **scaling and encoding** features.  

---

## 🤖 Models Evaluated

| Model                  | MAE (K) | RMSE (K) | R²   |
|-------------------------|---------|----------|------|
| Linear Regression       | ~46.0   | ~62.6    | 0.70 |
| Decision Tree (Best)    | ~36.7   | ~54.7    | 0.77 |
| Random Forest           | ~28.9   | ~44.0    | 0.85 |
| XGBoost                 | 27.1    | 40.5     | 0.877|
| **Stacking Ensemble**   | 26–28   | 39–41    | 0.88–0.89 |

✅ **Best Model:** Stacking Ensemble (XGB + RF + Ridge)

---

## 📈 Final Evaluation (Test Set)

- **XGBoost**
  - MAE ≈ 27K  
  - RMSE ≈ 40K  
  - R² ≈ 0.877  

- **Stacking Ensemble**
  - MAE ≈ 26K–28K  
  - RMSE ≈ 39K–41K  
  - R² ≈ 0.88–0.89  

---

## 📊 Visual Insights
- 📊 **Barplot**: MAE, RMSE, and R² comparison across models.  
- 📦 **Boxplot**: Error distributions → XGBoost & Stacking more stable with fewer outliers.  

---

## 🎯 Conclusions & Recommendations
- **Selected Model:** Stacking Ensemble (XGB + RF + Ridge)  
- **Why?**
  - Best trade-off between bias & variance.  
  - More stable across cross-validation folds.  
  - Scalable for larger datasets.  

### 🔮 Next Steps
- Deploy the **Stacking Ensemble** as a production model.  
- Retrain quarterly with updated data.  
- Expose the model via an **API** for real-time predictions.  

---

## 📁 Deliverables
- ✅ Trained models (`.pkl` files)  
- ✅ Performance metrics report (CSV)  
- ✅ Plots for comparison & error distributions  
- ✅ Executive project report (this document)  

---

## 🛠️ Tech Stack
- Python (Pandas, NumPy, Scikit-learn, XGBoost)  
- Matplotlib / Seaborn for static visualizations  
- Jupyter Notebook for analysis & reporting  


   

