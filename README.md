
# Analyzing the Spotify Dataset — Listener's Dataset

This repo contains a small, **synthetic** Spotify listener dataset (50 users) and ready-to-run Python code to analyze engagement, segments, and retention-like behavior.

## Project Structure
```text
.
├── data/
│   └── listeners_50.csv
├── outputs/                # figures will be saved here after running
├── src/
│   ├── __init__.py
│   ├── analysis.py
│   ├── viz.py
│   └── main.py
├── requirements.txt
└── README.md
```

## Quickstart
1. **Create & activate a virtual env (recommended)**
   ```bash
   python -m venv .venv
   # Windows
   .venv\Scripts\activate
   # macOS/Linux
   source .venv/bin/activate
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the analysis**
   ```bash
   python -m src.main --data data/listeners_50.csv --outdir outputs
   ```

Figures will be saved to `outputs/` and key tables will print in the terminal.

## What’s in the dataset?
- `listener_id`: unique id
- `age`, `gender`, `country`
- `subscription_type`: Free, Premium, Student, Family
- `total_streams`, `minutes_listened`, `avg_session_length_min`, `skips_per_hour`
- `likes`, `playlists_created`
- `device`, `platform`
- `churned` (boolean), `monthly_fee_inr`, `ad_impressions`
- `date_joined`, `last_active_date`
- engineered fields (on load): `tenure_days`, `streams_per_day`, `minutes_per_stream`, `is_paying`, `join_year`

**Note**: All data is randomly generated for demonstration and does not represent real users.

## Reproducibility
- The CSV was generated with a fixed random seed for stable runs.

## Uploading to GitHub
1. Initialize the repo and commit:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Spotify Listener analysis with synthetic dataset"
   ```
2. Create a repo on GitHub, then add the remote and push:
   ```bash
   git branch -M main
   git remote add origin https://github.com/<your-username>/spotify-listeners-analysis.git
   git push -u origin main
  

