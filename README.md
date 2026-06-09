# 🐄 Udder Hygiene Streamlit Dashboard

A secure, client-specific Streamlit dashboard that automates udder hygiene reporting for dairy farm data. This project replaces manual Excel work and static reporting with an interactive dashboard that gives clients and internal teams faster access to hygiene trends, visit summaries, and farm-level insights.

## Project Summary

Udder hygiene scoring data is often collected in the field and reviewed manually through spreadsheets or static reports. This dashboard turns that workflow into a repeatable reporting system: data is cleaned, validated, organized by client, and displayed through an easy-to-use web interface.

The goal of this project is to reduce manual reporting time, improve data consistency, and make hygiene trends easier to understand for operational decision-making.

## Business Problem

Manual reporting workflows can be slow, repetitive, and prone to formatting or data-entry issues. For dairy health reporting, teams need a way to quickly understand:

- How hygiene scores changed across visits
- Which groups have higher or lower hygiene performance
- Whether data quality issues exist in the submitted records
- What clients should see without manually sending custom files each time

This dashboard addresses those needs through a secure, preloaded reporting experience.

## Key Features

- 🔐 **Client-specific login** using access codes stored through Streamlit secrets
- 📊 **Interactive hygiene visualizations** for trends, averages, and group rankings
- 📈 **Last-visit summaries** for quick review of most recent farm performance
- 🧼 **No manual client uploads** because dashboards are preloaded with client-specific data
- 🏷️ **Branded client interface** with support for logos and custom display names
- 📱 **Mobile-friendly dashboard layout** for easier field and client access
- ⚠️ **Data-quality flagging** for missing or invalid records
- 🧑‍💻 **Admin dashboard support** for internal review and workflow management

## Dashboard Links

### Client Demo Dashboard

Demo credentials:

```text
Client ID: qmps_mock_up
Access Code: milk2025
```

🔗 Demo Dashboard: https://qmps-mockup.streamlit.app

> This demo is for mockup and testing purposes only. Only valid credentials load the corresponding dashboard.

### Admin Dashboard

🔗 Admin Dashboard: https://udderdashboardapppy-dh6fmxmojvax2jgtkyfsoz.streamlit.app

## Tech Stack

| Area | Tools |
|---|---|
| Language | Python |
| App Framework | Streamlit |
| Data Processing | pandas |
| Visualization | Matplotlib |
| Deployment | Streamlit Cloud |
| Configuration | `.streamlit/secrets.toml` |
| Data Storage Pattern | Client-specific CSV/data files |

## Data Workflow

```text
Raw hygiene data
        ↓
Validation and cleaning
        ↓
Flag missing or invalid entries
        ↓
Exclude flagged rows from client-facing charts
        ↓
Retain flagged rows for admin review
        ↓
Generate client-specific dashboard views
```

## Data Handling Logic

- Missing or invalid entries are flagged for review
- Flagged rows are excluded from client-facing visualizations
- Flagged records are retained so internal users can review or impute them later
- Clients do not need to clean or upload files manually
- Each client view loads only the data tied to their credentials

## What This Project Demonstrates

This project shows my ability to build practical analytics and automation tools that support real operational workflows.

It demonstrates experience with:

- Python-based data cleaning and validation
- Dashboard development with Streamlit
- Client-specific access control patterns
- Turning spreadsheet workflows into web-based reporting systems
- Building user-facing tools for non-technical stakeholders
- Structuring data products around real business needs

## Local Setup

1. Clone the repository:

```bash
git clone https://github.com/AishahAbdulHakeem/Udder-Hygiene-Streamlit-Dashboard.git
cd Udder-Hygiene-Streamlit-Dashboard
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Add client data and assets:

```text
/data/
/assets/
```

4. Configure secrets:

```toml
[your_client_id]
name = "Your Display Name"
code = "yourAccessCode"
logo = "assets/your_logo.png"
data = "data/your_data.csv"
```

5. Run locally:

```bash
streamlit run app.py
```

## Future Improvements

- Add database-backed storage instead of static client CSV files
- Add automated file ingestion and scheduled report refreshes
- Add role-based admin permissions
- Add exportable PDF or Excel summaries
- Add automated anomaly detection for hygiene score trends
- Expand dashboard metrics beyond udder hygiene into additional farm health indicators

## About

Created by **Aishah Abdul-Hakeem** as a workflow optimization and reporting prototype for dairy health data.

This project reflects my broader career focus on **automation engineering, data engineering, analytics engineering, and operational reporting systems**.