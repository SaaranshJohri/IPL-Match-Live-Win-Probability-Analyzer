# IPL-Match-Live-Win-Probability-Analyzer
A machine learning project that predicts the real-time win probability of a cricket match using ball-by-ball IPL data. The model analyzes match progression, team dynamics, and game context to generate data-driven insights for live match scenarios.

## 🚀 Project Overview

This project focuses on building a sports analytics system that:

Predicts match outcomes during live gameplay
Uses historical IPL ball-by-ball data
Applies multiple machine learning models
Demonstrates the importance of match context and game dynamics
📊 Dataset
Source: IPL Ball-by-Ball Dataset (Kaggle)
Files used:
matches.csv
deliveries.csv
Data Includes:
Match details (teams, venue, winner)
Ball-by-ball events (runs, wickets, overs)
Match progression information

## ⚙️ Feature Engineering

The model uses both team-level and match-context features:

inning → match inning (1st or 2nd)
batting_team → batting team (encoded)
bowling_team → bowling team (encoded)
over, ball → match progression
batsman_runs, extra_runs, total_runs → runs per delivery
is_wicket → wicket indicator
cumulative_runs → runs scored till current ball
cumulative_wickets → wickets fallen till current ball
runs_left → runs required to win
balls_left → balls remaining
wickets_left → wickets remaining

##🧠 Models Used

Multiple machine learning algorithms were implemented and compared:

Logistic Regression
Decision Tree
Random Forest
Gradient Boosting
K-Nearest Neighbors (KNN)

## 📈 Model Performance
Model	            Accuracy
Decision Tree	      ~85%
Random Forest	      ~82–85%
Gradient Boosting	  ~65%
Logistic Regression	~56%
KNN	                ~72%

## Sample Prediction
sample = pd.DataFrame([[1,8,16,0,1,0,1,1,0,1,0,0,119,10]],
rf.predict_proba(sample)
Output - [0.2146, 0.7853]

## 👉 Interpretation:

21.4% → probability of losing
78.5% → probability of winning

## 🔍 Key Insights
Match context (runs required, wickets, pressure) is more important than team names
Tree-based models outperform linear models
Required Run Rate and Wickets Remaining are key predictors
Removing data leakage significantly improved model reliability

## 🛠 Tech Stack
Python
Pandas, NumPy
Scikit-learn
Matplotlib
Joblib

## 📌 Future Improvements
Add XGBoost for improved accuracy
Build Streamlit dashboard for live predictions
Integrate real-time match data
Add player-level performance analysis
Improve visualization and storytelling

## 💡 Learning Outcomes
Feature engineering for time-series sports data
Handling data leakage in ML pipelines
Model comparison and evaluation
Building interpretable sports analytics systems

## 📎 Use Cases
Sports broadcasting analytics
Live match insights
Fantasy sports strategy
Data storytelling in sports

## 👨‍💻 Author

Saaransh Johri
AI/ML Engineer | Software Developer

👉 Tree-based models performed best due to non-linear relationships in match conditions.
