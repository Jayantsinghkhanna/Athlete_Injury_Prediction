# Athlete_Injury_Prediction
Machine learning pipeline to predict injuries in collegiate athletes using training, performance, and demographic data, with model evaluation and feature analysis.

# Athlete Injury Analysis Pipeline

## 📖 Project Overview
This project implements a **full machine learning pipeline** to predict injuries in collegiate athletes. The pipeline includes:

- Data loading and cleaning  
- Exploratory Data Analysis (EDA)  
- Feature engineering and preprocessing  
- Training multiple machine learning models  
- Model evaluation and comparison  
- Saving the best-performing model for deployment  

The goal is to help coaches and trainers identify risk factors for athlete injuries and make informed decisions to improve player safety and performance.

---

## 🗂 Dataset
The dataset `collegiate_athlete_injury_dataset.csv` contains information about collegiate athletes, including physical measurements, training patterns, performance, and injury history.

### Columns:
- **Demographics:** `Age`, `Gender`, `Position`, `Height_cm`, `Weight_kg`  
- **Training metrics:** `Training_Intensity`, `Training_Hours_Per_Week`, `Recovery_Days_Per_Week`, `Match_Count_Per_Week`  
- **Performance metrics:** `Fatigue_Score`, `Performance_Score`, `Team_Contribution_Score`, `Load_Balance_Score`  
- **Target variable:** `Injury_Indicator` (0 = No injury, 1 = Injury)

---

## 🔍 Exploratory Data Analysis (EDA)
- Checked for missing values, duplicates, and unique counts.  
- Visualized numeric distributions with histograms and KDE plots.  
- Correlation heatmap to identify relationships between features and injury risk.  
- Countplots to see distribution of **Position** and **Injury_Indicator** by **Gender**.  
- Barplots and scatterplots to explore relationships between training metrics, fatigue, performance, and injury incidence.

---

## ⚙️ Data Preprocessing
Before training models, the following preprocessing steps were applied:

1. **Categorical encoding:**
   - `Gender`: Male = 0, Female = 1  
   - `Position`: Guard = 0, Center = 1, Forward = 2  

2. **Feature scaling:**  
   - All numerical features scaled using `StandardScaler` for normalization.  

3. **Selected features for modeling:**
   ```text
   Age, Gender, Position, Height_cm, Weight_kg,
   Training_Intensity, Training_Hours_Per_Week,
   Recovery_Days_Per_Week, Match_Count_Per_Week,
   Fatigue_Score, Performance_Score,
   Team_Contribution_Score, Load_Balance_Score

   🤖 Applied Machine Learning Models

The pipeline applies multiple models to compare performance:

Random Forest Classifier

Tree-based ensemble model

Feature importance visualizations

Logistic Regression

Baseline linear classifier

Useful for understanding feature coefficients

Gradient Boosting Classifier

Boosted decision trees for high accuracy

Robust to overfitting

Support Vector Classifier (SVC)

Kernel-based classifier

Captures non-linear decision boundaries

Metrics reported for all models:

Accuracy

Mean Squared Error (MSE)

Mean Absolute Error (MAE)

Classification Report (Precision, Recall, F1-score)

Feature importance (for tree-based models)
