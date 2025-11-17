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


# Setting up your Machine and Project
Complete each step in the following guide and verfiy carefully.
- [Setup Machine](SET_UP_MACHINE.md)

After your machine is set up, set up a new Python project by copying this template. Complete each step in the following guide.
- [Setup Project](SET_UP_PROJECT.md)

It includes the critical commands to set up your local environment (and activate it):
('
uv venv
uv python pin 3.12
uv sync --extra dev --extra docs --upgrade
uv run pre-commit install
uv run python --version
Windows (PowerShell):
')
('
.\.venv\Scripts\activate
macOS / Linux / WSL:
')
('
source .venv/bin/activate
')
# Daily Workflow
Please ensure that the prior steps have been verified before continuing. When working on a project, we open just that project in VS Code.

## Git Pull from GitHub
Always start with git pull to check for any changes made to the GitHub repo.

git pull

## Run Checks as You Work
This mirrors real work where we typically:

Update dependencies (for security and compatibility).
Clean unused cached packages to free space.
Use git add . to stage all changes.
Run ruff and fix minor issues.
Update pre-commit periodically.
Run pre-commit quality checks on all code files (twice if needed, the first pass may fix things).
Run tests.
In VS Code, open your repository, then open a terminal (Terminal / New Terminal) and run the following commands one at a time to check the code.

uv sync --extra dev --extra docs --upgrade
uv cache clean
git add .
uvx ruff check --fix
uvx pre-commit autoupdate
uv run pre-commit run --all-files
git add .
uv run pytest
NOTE: The second git add . ensures any automatic fixes made by Ruff or pre-commit are included before testing or committing.



## Build Project Documentation
Make sure you have current doc dependencies, then build your docs, fix any errors, and serve them locally to test.

uv run mkdocs build --strict
uv run mkdocs serve
After running the serve command, the local URL of the docs will be provided. To open the site, press CTRL and click the provided link (at the same time) to view the documentation. On a Mac, use CMD and click.
Press CTRL c (at the same time) to stop the hosting process.

## Execute
This project includes demo code. Run the demo Python modules to confirm everything is working.

In VS Code terminal, run:

uv run python -m analytics_project.demo_module_basics
uv run python -m analytics_project.demo_module_languages
uv run python -m analytics_project.demo_module_stats
uv run python -m analytics_project.demo_module_viz
You should see:

Log messages in the terminal
Greetings in several languages
Simple statistics
A chart window open (close the chart window to continue).
If this works, your project is ready! If not, check:

Are you in the right folder? (All terminal commands are to be run from the root project folder.)
Did you run the full uv sync --extra dev --extra docs --upgrade command?
Are there any error messages? (ask for help with the exact error)

## Git add-commit-push to GitHub
Anytime we make working changes to code is a good time to git add-commit-push to GitHub.

Stage your changes with git add.
Commit your changes with a useful message in quotes.
Push your work to GitHub.
git add .
git commit -m "describe your change in quotes"
git push -u origin main
This will trigger the GitHub Actions workflow and publish your documentation via GitHub Pages.

## Modify and Debug
With a working version safe in GitHub, start making changes to the code.

Before starting a new session, remember to do a git pull and keep your tools updated.

Each time forward progress is made, remember to git add-commit-push.


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

- Distribution of game-level scoring

- Correlations between performance metrics

- Relationship between minutes and scoring

- Top scoring players of 2025

- Rolling player trends

- Shot efficiency vs. scoring output

- All visualizations are generated using Matplotlib.

# 🤖 4. Machine Learning Modeling

Two models were implemented:

Model 1 — Linear Regression

- Used as a baseline scoring prediction model.

Model 2 — Random Forest Regressor

- Advanced model used as the primary predictive method.

Metrics compared:

- R²

- RMSE

- MAE

Random Forest consistently produced higher performance.


# ▶️ 5. How to Run the Notebook
1. Clone the repository
git clone https://github.com/mindy0cruz/wnba-capstone.git
cd wnba-capstone

2. Install dependencies
pip install -r requirements.txt

3. Open the notebook
jupyter notebook notebooks/wnba.ipynb

# 📘 6. Project Goals

This project investigates:

Key Question:

- What factors most strongly influence WNBA player scoring performance in the 2025 season?

Dependent Variable:

points (game-level scoring)

Independent Variables:

- Minutes played

- Shooting percentages

- Assists, rebounds, steals, blocks

- Turnovers

- Win/loss

- Team context

# 📄 7. Deliverables

✔ Jupyter Notebook (wnba.ipynb)
✔ Cleaned dataset
✔ Machine learning modeling
✔ Visualizations and EDA
✔ Streamlit app
✔ Full LaTeX report (Overleaf)
