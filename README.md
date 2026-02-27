<div align="center">
  <img src="docs/assets/consumer360-banner.svg" alt="Consumer360 Banner" width="100%" />

  # Consumer360
  ### Production Retail Intelligence Platform

  [![Python](https://img.shields.io/badge/Python-3.11+-3776AB?logo=python&logoColor=white)](https://www.python.org/)
  [![FastAPI](https://img.shields.io/badge/FastAPI-0.116-009688?logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
  [![React](https://img.shields.io/badge/React-18-20232A?logo=react&logoColor=61DAFB)](https://react.dev/)
  [![Vite](https://img.shields.io/badge/Vite-7-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/)
  [![License](https://img.shields.io/badge/License-MIT-green.svg)](#license)
</div>

## Vision
Consumer360 turns raw retail transactions into real-time growth decisions:
- Identify **Champions** for premium campaigns
- Detect **Churn Risk** customers early for retention workflows
- Deliver **weekly auto-refresh intelligence** for business teams

## Product Highlights
- `RFM Segmentation`: Automated 1-5 scoring + segment labeling
- `CLV Modeling`: Predictive lifetime value via `lifetimes`
- `Cohort Retention`: Monthly retention matrix for behavior trend analysis
- `Market Basket Analysis`: Association rules for cross-sell opportunities
- `Data Quality Guardrails`: Built-in validation report before publishing outputs
- `Executive Dashboard`: Advanced light-theme React UI with filters, spotlight search, insight cards, and campaign priority queue
- `API Layer`: FastAPI endpoints for KPI/payload/campaign integrations

## Architecture
```text
SQL (schema + cleansing)
   -> Python Analytics Core (RFM, Cohort, CLV, Basket, Quality)
   -> Reports + Frontend Payload JSON
   -> React Command Center + FastAPI Service
```

## Screens and UX
- Sidebar command panel (region / segment / month window)
- Revenue and segment performance visuals
- Customer spotlight lookup
- Strategic AI-style insight cards
- Campaign priority scoring table
- One-click CSV exports for action lists

## Quick Start
### 1. Install
```powershell
pip install -r requirements.txt
```

### 2. Run Analytics Pipeline
```powershell
python -m src.main --run-date 2026-02-27
```

### 3. Launch Frontend
```powershell
./run_frontend.ps1
```
Frontend URL: `http://localhost:5173`

### 4. Launch API
```powershell
./run_api.ps1
```
Swagger docs: `http://127.0.0.1:8000/docs`

## One-Command Flow
```powershell
./run_consumer360.ps1 -RunDate 2026-02-27 -LaunchFrontend -LaunchApi
```

## API Endpoints
- `GET /health`
- `GET /payload`
- `GET /kpis`
- `GET /campaigns`
- `GET /quality`

## Generated Outputs
- `reports/data_quality_report.json`
- `reports/customer_rfm_segments.csv`
- `reports/customer_clv.csv`
- `reports/cohort_retention.csv`
- `reports/market_basket_rules.csv`
- `reports/campaign_champions.csv`
- `reports/campaign_churn_risk.csv`
- `frontend/public/data/dashboard_payload.json`

## Repository Structure
```text
api/                FastAPI service
config/             Runtime + brand settings
docs/               Architecture and runbooks
frontend/           React + Vite dashboard
reports/            Generated analytics outputs
sql/                Schema and SQL analytics scripts
src/                Python analytics pipeline
```

## Roadmap
- Authentication + role-based dashboards
- PDF executive report export
- Scenario simulator for campaign budget allocation
- Cloud deployment templates (Docker + CI/CD)

## License
MIT
