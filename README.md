# FlavorGraph Recipe Generator

Recipe Suggester is an intelligent web application that helps users discover dishes based on the ingredients they have. Built with Python Flask, SQLite, and modern HTML/CSS/JS, it leverages graph theory, backtracking, and greedy algorithms to efficiently match recipes, analyze ingredient gaps, and suggest substitutions for missing items.

✨ Features

 Suggest recipes based on available ingredients

 Supports regional cuisines: Telugu, Gujarati, Marathi (extendable to more)

 Ingredient gap analysis — see what’s missing for each recipe

 Smart substitution engine (direct, category, fuzzy matches)

 Modern frontend with chip-based ingredient entry and responsive results UI

 Shopping list aggregation from suggested recipes

 Fully extensible database (seed_db.py makes adding new recipes simple)

🛠️ Tech Stack

Backend: Python 3, Flask

Database: SQLite3

Frontend: HTML5, CSS3, JavaScript

Algorithms: Graph theory, Greedy search, Backtracking

Deployment: Flask (local), optional Dockerfile

📂 Project Structure









<img width="542" height="376" alt="image" src="https://github.com/user-attachments/assets/145f481a-8e65-43e3-a32b-ab67fa089b6d" />

🚀 Getting Started

Create & activate a virtual environment

python -m venv venv
# On Windows
venv\Scripts\activate
# On Mac/Linux
source venv/bin/activate


Install dependencies

pip install -r requirements.txt


Seed the database

python seed_db.py


Run the Flask app

python app.py


Open your browser at 👉 http://127.0.0.1:5000

🍛 Adding Recipes

Recipes are added in seed_db.py and include:

name

cuisine (Telugu, Gujarati, Marathi, etc.)

servings

instructions


Example in seed_db.py:

recipes = [
    ("Pulihora", "Telugu", 3, "Cook rice, mix with tamarind paste.", "/static/images/pulihora.jpg"),
    ("Undhiyu", "Gujarati", 4, "Mixed vegetables cooked in spices.", "/static/images/undhiyu.jpg")
]

⚙️ How Algorithms Work
1. Greedy Algorithm (Default)

Quickly finds recipes that best match available ingredients.

Uses graph-enhanced scoring to prioritize ingredient combinations that commonly appear together.

Fast and ideal for partial ingredient sets.

Output includes missing ingredients and substitutions.

2. Backtracking Algorithm

Finds exact combinations of recipes that use all available ingredients.

Optimal for precise ingredient usage, but slower for large datasets.

Falls back to greedy if no exact match is found.

3. Graph Theory

Builds a graph of ingredients co-occurring in recipes.

Enhances recipe scores and suggests complementary ingredients.

Makes suggestions smarter and more aligned with real-world cooking patterns.

🔧 Extending the App

Add new recipes to seed_db.py and rerun to update the database.

Add new cuisines or categories as needed.

Enhance substitution rules in substitution.py for more intelligent suggestions.

Improve UI styling in static/styles.css and templates.

Sample Results
<img width="1432" height="823" alt="image" src="https://github.com/user-attachments/assets/aff5e5b4-8023-42f6-8f6a-803ab526f10b" />
<img width="1602" height="892" alt="image" src="https://github.com/user-attachments/assets/48630d57-a926-4b40-9c7f-f4e4c9ef230a" />

