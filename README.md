# ⚽🏆 WinFPL - Fantasy Premier League Analytics/Live Dashboard

**WinFPL** is an interactive datadashboard for Fantasy Premier League managers that combines live FPL API data, player performance trends, fixture difficulty, and a lightweight prediction model to support better transfer, lineup, and captaincy decisions. The project demonstrates data collection, feature engineering, dashboard design, exploratory analysis, and predictive analytics in a real-world sports analytics use case.


## Business Problem

Fantasy Premier League managers often need to make weekly decisions under time pressure using scattered data points such as player form, price, fixture difficulty, and expected returns. This project brings those signals together into one dashboard to make player comparison and decision-making faster and more data-driven.


## Live Demo

[Deployed on Streamlit Cloud](https://winfplwithml.streamlit.app/)


## Data Source

The dashboard uses live data from the official Fantasy Premier League API, including:
- Player statistics
- Team information
- Fixture schedules
- Historical performance data

The data is transformed into analytics-friendly features such as recent form, points-per-million, fixture difficulty, and predicted next-gameweek output.


## Features

- Live FPL data for players, teams, fixtures, and performance history
- Interactive filters by team, position, price, form, and predicted points
- Advanced metrics such as 3GW form, fixture difficulty, PPM, and age-adjusted views
- Interactive Plotly visualizations including scatter plots, treemaps, and comparison charts
- Captaincy heatmap to highlight strong predicted performers
- Lightweight RandomForest model for next gameweek point estimation


## Key Insights

This dashboard helps answer questions such as:
- Which players offer strong recent form at a lower price point?
- Which captaincy choices combine good form with favorable fixtures?
- Which players may be overvalued or undervalued based on output trends?
- How do position, price, and upcoming fixtures affect expected performance?


## Predictive Model

A RandomForest model is used to estimate next gameweek points based on recent performance and engineered features. The model is intended as a supporting decision tool rather than a high-precision forecasting system, helping rank players and surface useful short-term signals.


## Tech Stack

Python | Streamlit | Pandas | Plotly | Scikit-learn | FPL API


## Model Performance

| Metric | Value |
| RMSE | ~2.7 |
| MAE | ~2.0 |
| R² | 0.15 |


## Quick Start (Local)

```bash
python -m venv .venv
pip install -r requirements.txt
streamlit run winfpl.py
```


## File Structure

```text
├── winfpl.py          # Main Streamlit app
├── requirements.txt   # Dependencies
└── README.md          # Project documentation
```


## Limitations

- The prediction model has limited explanatory power and should be used as a directional aid.
- FPL outcomes are noisy and affected by many match-specific factors not fully captured in the model.
- The dashboard is strongest for short-term comparison and decision support, not long-range forecasting.



Built by Jwel Sharma for FPL managers & data science portfolio. ⭐
