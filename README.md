# video-games-sales-prediction
🎮 Video Games Sales Prediction
📌 Project Overview

Video Games Sales Prediction is a Machine Learning project that predicts the global sales of video games using historical video game data.

The project analyzes factors such as platform, genre, critic score, user score, rating, and other attributes to identify patterns that influence video game sales. Multiple regression algorithms are trained, tuned, and evaluated to select the best-performing model.

🎯 Objectives
Predict global video game sales using Machine Learning.
Analyze the factors that influence video game sales.
Preprocess and transform real-world sales data.
Compare multiple regression algorithms.
Optimize models using Grid Search and 5-Fold Cross-Validation.
Select the best model based on RMSE and R² Score.
📊 Dataset

The dataset contains 16,598 video game records scraped from VGChartz.

Important Features
Platform – Gaming platform
Year – Release year
Genre – Game genre
Publisher – Game publisher
Rating – Age/content rating
Critic_Score – Professional critic score
Critic_Count – Number of critic reviews
User_Score – Player rating
User_Count – Number of user ratings
Global_Sales – Worldwide sales in millions (Target Variable)

Dataset source:
https://www.kaggle.com/datasets/gregorut/videogamesales

🔄 Project Workflow
Dataset
   ↓
Data Preprocessing
   ↓
Feature Engineering
   ↓
Categorical Encoding
   ↓
Z-Score Normalization
   ↓
Log Transformation
   ↓
Train-Test Split (80:20)
   ↓
Model Training
   ↓
5-Fold Cross-Validation
   ↓
Hyperparameter Tuning
   ↓
Model Evaluation
   ↓
Best Model Selection
🧹 Data Preprocessing

The following preprocessing techniques were applied:

Missing numerical values were replaced using mean imputation.
Missing categorical values were handled using mode imputation.
Irrelevant attributes such as Name and Rank were removed.
Age of the Game was derived from the release year.
Categorical features were encoded using Label Encoding.
Numerical features were scaled using Z-Score Normalization.
Global_Sales was transformed using log1p to handle its highly skewed distribution.
🤖 Machine Learning Models

Five regression algorithms were implemented:

K-Nearest Neighbour (KNN) Regressor
Linear Regression
Support Vector Regressor (SVR)
Random Forest Regressor
XGBoost Regressor

The dataset was divided into an 80:20 train-test split, and 5-fold cross-validation was used for hyperparameter optimization.

⚙️ Hyperparameter Tuning

Grid Search was used to find suitable hyperparameters for the regression models.

The tuning process helps improve model performance and ensures that the selected model generalizes better to unseen data.

📈 Evaluation Metrics

The models were evaluated using:

R² Score

Measures how much of the variance in the target variable can be explained by the model.

Higher R² = Better performance

RMSE

Measures the average magnitude of prediction errors.

Lower RMSE = Better performance

🏆 Results

The XGBoost Regressor achieved the best overall performance.

Metric	XGBoost
R² Score	0.6528
RMSE	0.2885

The model explains approximately 65.3% of the variance in the log-transformed global sales and achieved the lowest RMSE among the evaluated models.

🔍 Feature Importance

Feature importance analysis using the Random Forest model showed that:

User_Count
Critic_Score

were among the most influential features for predicting global video game sales.

🛠️ Technologies Used
Python
Pandas
NumPy
Scikit-Learn
XGBoost
Matplotlib
Machine Learning
Regression Algorithms
📁 Project Structure
Video-Games-Sales-Prediction/
│
├── dataset/
│   └── vgsales.csv
│
├── notebooks/
│   └── Video_Game_Sales_Prediction.ipynb
│
├── README.md
│
└── Documentation.pdf

The exact folder structure may vary depending on the files included in the repository.

🚀 Future Scope

The project can be further improved by:

Incorporating social media sentiment and pre-release hype data.
Exploring Deep Learning models such as RNN and LSTM.
Predicting sales separately for different regions.
Using additional game-related features to improve prediction accuracy.

These extensions are also suggested in the project documentation.

📚 References
Kaggle Video Games Sales Dataset:
https://www.kaggle.com/datasets/gregorut/videogamesales
Scikit-Learn Documentation:
https://scikit-learn.org/stable/
