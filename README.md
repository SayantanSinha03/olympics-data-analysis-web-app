# 🏅 Olympics Data Analysis Web App

An interactive Streamlit web application for exploring 120 years of Olympic history — from medal tallies and country performance to athlete demographics and gender participation trends.

🔗 **Live App:** [olympics-data-analysis-web-app-yvevfzrs6iemjsxnsbr7qb.streamlit.app](https://olympics-data-analysis-web-app-yvevfzrs6iemjsxnsbr7qb.streamlit.app/)
📊 **Dataset:** [120 Years of Olympic History (Kaggle)](https://www.kaggle.com/heesoo37/120-years-of-olympic-history-athletes-and-results)

## Author

**Sayantan Sinha**
B.E. in Information Technology | ML Enthusiast | Python Developer

🔗 [GitHub](https://github.com/SayantanSinha03)

## Overview

This app lets users interactively explore Olympic Games data across editions, countries, sports, and individual athletes — turning ~270,000 rows of raw athlete-event data into filterable tables and interactive visualizations.

## Features

**🥇 Medal Tally**
Filter medal counts by year, country, or both to see overall standings or how a specific nation performed.

**📈 Overall Analysis**
- Key stats: number of editions, host cities, sports, events, athletes, and participating nations
- Trends of participating nations, events, and athletes over time
- A sport-vs-year heatmap showing how the number of events per sport evolved
- Most successful athletes, filterable by sport

**🌍 Country-wise Analysis**
- Year-by-year medal tally for a selected country
- Heatmap of which sports that country performs best in
- Top 10 athletes for the selected country

**🏃 Athlete-wise Analysis**
- Age distribution of medalists overall and by individual sport
- Height vs. weight scatter plot by sport, colored by medal type
- Men vs. women participation trends over the years

## Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| Web Framework | Streamlit |
| Data Processing | Pandas, NumPy |
| Visualization | Plotly, Matplotlib, Seaborn, SciPy |

## How It Works

Raw athlete-event and NOC-region datasets are merged and cleaned in `preprocessor.py`. Reusable aggregation logic — medal tallies, year-wise trends, country/sport breakdowns — lives in `helper.py`. `app.py` ties everything together into a sidebar-driven interface, so every chart and table updates dynamically based on user selections, without reloading the page.

## Run Locally

```bash
git clone https://github.com/SayantanSinha03/olympics-data-analysis-web-app.git
cd olympics-data-analysis-web-app
python -m venv venv
.\venv\Scripts\Activate.ps1
pip install -r requirements.txt
streamlit run app.py
```

## Project Structure

```
├── app.py              # Main Streamlit app and page routing
├── helper.py            # Data aggregation and analysis functions
├── preprocessor.py       # Data cleaning and merging
├── requirements.txt      # Python dependencies
├── runtime.txt           # Pinned Python version for deployment
├── athlete_events.csv     # Raw dataset
└── noc_regions.csv        # NOC-to-country mapping
```