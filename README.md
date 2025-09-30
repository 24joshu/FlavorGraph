
# Recipe Suggester

An intelligent recipe suggestion web app built with Python Flask + SQLite + HTML/CSS/JS, that helps users discover dishes based on the ingredients they have.

It leverages graph theory, backtracking, and greedy algorithms to efficiently match recipes, analyze ingredient gaps, and even suggest substitutions for missing ingredients.

## How to run

1. Create a virtualenv (optional):
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

2. Run the app:
   ```bash
   python seed_db.py
   python app.py
   ```

3. Open http://localhost:5000 in your browser.

## What is included

- `app.py` — Flask app
- `recipe_matching.py` — core matching logic
- `substitution.py` — substitution lookup
- `templates/index.html` — simple frontend
- `static/styles.css` — basic styling
- `data/recipes.db` — seeded SQLite DB

✨ Features

 --> Suggest recipes based on available ingredients
 --> Supports regional cuisines: Telugu, Gujarati, Marathi (extendable to more)
 --> Ingredient gap analysis — see what’s missing
 --> Smart substitution engine (direct, category, fuzzy matches)
 --> Photos for recipes (local or URL-based)
 --> Modern frontend with chip-based ingredient entry and results UI
 --> Shopping list aggregation from suggested recipes
 --> Fully extensible database (seed_db.py makes it easy to add new recipes

🛠️ Tech Stack

Backend: Python 3, Flask

Database: SQLite3

Frontend: HTML5, CSS3, Vanilla JS

Algorithms: Graph theory, Backtracking, Greedy search

Deployment: Flask (local), optional Dockerfile

📂 Project Structure









<img width="658" height="427" alt="image" src="https://github.com/user-attachments/assets/42fb4629-2f0d-4fa6-a1c6-a153294b3cd7" />


Results
<img width="1523" height="903" alt="image" src="https://github.com/user-attachments/assets/c81039e1-81cf-43fb-b6ae-d30ad9583669" />
<img width="1443" height="821" alt="image" src="https://github.com/user-attachments/assets/5031c8f4-6fdd-4fd0-bdbe-87529b4c05cd" />





