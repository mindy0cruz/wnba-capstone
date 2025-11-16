# 📊 WNBA 2025 Player Performance Analysis
Predicting Player Scoring Using Machine Learning

This project analyzes WNBA 2025 player box score data and builds a machine learning model to predict player scoring performance. The project includes full data cleaning, exploratory data analysis (EDA), feature engineering, model comparison, and an optional interactive Streamlit app for real-time predictions.

The project satisfies the full capstone requirements:
✔ Data collection
✔ Professional data description
✔ Cleaning & preprocessing
✔ EDA and visualization
✔ Predictive modeling
✔ Reporting & GitHub repository
✔ Advanced component (Random Forest)

📁 Project Structure
wnba-capstone/
Need to lay this out here

# 📥 1. Data Source

This project uses the player box score dataset for the 2025 WNBA season, obtained from the open-source:

🔗 SportsDataverse WeHoop WNBA Data Repository
https://github.com/sportsdataverse/wehoop-wnba-data

Dataset Used: player_box_2025.csv
Records: ~4,700 player-game rows
Attributes: 16 cleaned and feature-engineered performance fields

# 🧼 2. Data Cleaning & Preparation

The notebook performs:

Import and inspection of raw CSV

Type correction (numeric → float/int)

Duplicate removal

Handling missing shooting percentages

Replace with player season averages

For first-game players → fill with zero

Creation of engineered features:

win (0/1)

Rolling average points

Outlier checks and filtering

Final cleaned dataset with 16 essential features

A complete cleaning workflow diagram is included in the Overleaf report.

# 🔍 3. Exploratory Data Analysis (EDA)

The notebook explores:

Distribution of game-level scoring

Correlations between performance metrics

Relationship between minutes and scoring

Top scoring players of 2025

Rolling player trends

Shot efficiency vs. scoring output

All visualizations are generated using Matplotlib.

# 🤖 4. Machine Learning Modeling

Two models were implemented:

Model 1 — Linear Regression

Used as a baseline scoring prediction model.

Model 2 — Random Forest Regressor

Advanced model used as the primary predictive method.

Metrics compared:

R²

RMSE

MAE

Random Forest consistently produced higher performance.


# ▶️ 5. How to Run the Notebook
1. Clone the repository
git clone https://github.com/mindy0cruz/wnba-capstone.git
cd wnba-capstone

2. Install dependencies
pip install -r requirements.txt

3. Open the notebook
jupyter notebook notebooks/wnba.ipynb

📘 6. Project Goals

This project investigates:

Key Question

What factors most strongly influence WNBA player scoring performance in the 2025 season?

Dependent Variable

points (game-level scoring)

Independent Variables

Minutes played

Shooting percentages

Assists, rebounds, steals, blocks

Turnovers

Win/loss

Team context

# 📄 7. Deliverables

✔ Jupyter Notebook (wnba.ipynb)
✔ Cleaned dataset
✔ Machine learning modeling
✔ Visualizations and EDA
✔ Streamlit app
✔ Full LaTeX report (Overleaf)
