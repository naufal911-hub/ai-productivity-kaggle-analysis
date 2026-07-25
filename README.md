AI Usage & Productivity Analysis

An exploratory analysis of the relationship between AI tool usage and productivity, using a dataset from Kaggle.

Goal

To examine whether, and how strongly, AI usage correlates with productivity outcomes in the dataset, and to surface any interesting patterns along the way (e.g. by role, frequency of use, or task type, depending on what the data supports).

Dataset
Source: https://www.kaggle.com/datasets/ashyou09/global-ai-usage-and-productivity/data
Not included in this repo (see .gitignore), download it from the link above and place it in a data/ folder to reproduce the analysis.
Contents
analysis-notebook/ — main notebook(s): data cleaning, exploration, and correlation analysis
docker-compose.yml — spins up the full stack, no local install needed:
database — PostgreSQL, holds the working dataset
admin-gui — pgAdmin, for inspecting/querying the database visually
code-editor — Jupyter (datascience-notebook), where the analysis happens
Status

Work in progress. Currently focused on exploratory data analysis; correlation modeling and findings to follow.

Running

Requires Docker and Docker Compose installed. No manual dependency installation needed, everything runs in the containers.

Create a .env file in the project root with:
   POSTGRES_USER=your_user
   POSTGRES_PASSWORD=your_password
   POSTGRES_DB=your_db
   PGADMIN_DEFAULT_EMAIL=your_email@example.com
   PGADMIN_DEFAULT_PASSWORD=your_password
Start the stack:
bash
   docker compose up
Access:
Jupyter: http://localhost:8888 (no token/password required)
pgAdmin: http://localhost:80
