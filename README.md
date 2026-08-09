# 🏅 Olympics Data Analysis Web App

An interactive Streamlit web application for exploring 120 years of Olympic history — from medal tallies and country performance to athlete demographics and gender participation trends.

🔗 **Live App:** [Add your Streamlit Cloud link here once deployed]
📊 **Dataset:** [120 Years of Olympic History (Kaggle)](https://www.kaggle.com/heesoo37/120-years-of-olympic-history-athletes-and-results)

## Overview

This app lets users interactively explore Olympic Games data across editions, countries, sports, and individual athletes. It combines data preprocessing, visualization, and an intuitive Streamlit interface to surface trends that would otherwise be buried in raw CSV data.

## Features

- **Medal Tally** — Filter medal counts by year, country, or both
- **Overall Analysis** — Key stats (editions, hosts, sports, events, athletes, nations), trends of participating nations/events/athletes over time, and a sport-vs-year heatmap of event growth
- **Country-wise Analysis** — Year-by-year medal performance for a selected country, plus a heatmap of which sports that country excels in
- **Athlete-wise Analysis** — Age distribution of medalists overall and by sport, height vs. weight scatter plots by sport, and a men vs. women participation trend over the years

## Tech Stack

- **Python**
- **Streamlit** — web app framework
- **Pandas / NumPy** — data preprocessing and aggregation
- **Plotly** — interactive line charts and distribution plots
- **Matplotlib / Seaborn** — heatmaps and scatter plots

## How It Works

Raw athlete-event and NOC-region datasets are merged and cleaned in `preprocessor.py`, with reusable aggregation logic (medal tallies, year-wise trends, country/sport breakdowns) handled in `helper.py`. `app.py` ties it together into a sidebar-driven Streamlit interface, so every chart and table updates dynamically based on user selections.

## Run Locally

```bash
git clone https://github.com/SayantanSinha03/olympics-data-analysis-web-app.git
cd olympics-data-analysis-web-app
python -m venv venv
.\venv\Scripts\Activate.ps1
pip install -r requirements.txt
streamlit run app.py
```