<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0B4F7D,40:0C7196,100:14B8A6&height=220&section=header&text=Consumer360&fontSize=56&fontColor=ffffff&desc=Production-Ready%20Retail%20Intelligence%20Platform&descSize=18&descAlignY=68" alt="Consumer360 Hero" width="100%" />

  <h1>Consumer360</h1>
  <p><b>Production-Ready Retail Intelligence Platform</b></p>
  <p><i>Customer Segmentation • CLV Intelligence • Retention Analytics • Campaign Actioning</i></p>

  <p>
    <img src="https://img.shields.io/badge/Python-3.11+-3776AB?logo=python&logoColor=white" />
    <img src="https://img.shields.io/badge/FastAPI-0.116-009688?logo=fastapi&logoColor=white" />
    <img src="https://img.shields.io/badge/React-18-20232A?logo=react&logoColor=61DAFB" />
    <img src="https://img.shields.io/badge/Vite-7-646CFF?logo=vite&logoColor=white" />
    <img src="https://img.shields.io/badge/Analytics-RFM%20%7C%20CLV%20%7C%20Cohort-orange" />
  </p>

  <p>
    <a href="#product-preview">Preview</a> •
    <a href="#architecture-snapshot">Architecture</a> •
    <a href="#quick-start">Quick Start</a> •
    <a href="#api-endpoints">API</a>
  </p>
</div>

---

## Product Preview
<table>
  <tr>
    <td><b>Executive Dashboard</b><br/>Light premium UI with sidebar control center, KPI strips, charts, spotlight search, and campaign queue.</td>
    <td><b>Action Engine</b><br/>One-click exports for Champions and Churn Risk lists, ready for marketing and retention teams.</td>
  </tr>
  <tr>
    <td><b>Analyst Friendly</b><br/>Deep sections for cohort retention, CLV leaderboard, and market basket opportunities.</td>
    <td><b>Business Ready</b><br/>Weekly refresh pipeline + quality checks + API for integrations.</td>
  </tr>
</table>

## Architecture Snapshot
```mermaid
flowchart LR
    A[SQL Layer<br/>Schema + Cleansing + Cohort SQL] --> B[Python Analytics Core<br/>RFM + CLV + MBA + Quality Checks]
    B --> C[Reports + Dashboard Payload JSON]
    C --> D[React Executive Dashboard]
    C --> E[FastAPI Service]
    E --> F[Integrations / Automation]
```

## Why Consumer360
<table>
  <tr>
    <td><b>Champion Discovery</b><br/>Automatically identifies high-value customers for premium engagement.</td>
    <td><b>Churn Risk Prevention</b><br/>Builds action lists to prioritize retention interventions weekly.</td>
  </tr>
  <tr>
    <td><b>Advanced Analytics Stack</b><br/>RFM + CLV + Cohort + Market Basket in a single product workflow.</td>
    <td><b>Business-Ready Delivery</b><br/>Dashboard + API + exports + automation scripts included.</td>
  </tr>
</table>

## Core Capabilities
- **RFM Segmentation Engine**: 1-5 scoring with segment labels (Champions, At Risk, Hibernating, etc.)
- **Predictive CLV**: BG/NBD + Gamma-Gamma modeling via `lifetimes`
- **Cohort Retention Matrix**: Month-wise retention trends for behavioral analysis
- **Market Basket Rules**: Cross-sell associations using support/confidence/lift
- **Data Quality Guardrails**: Validates transaction quality before publishing outputs
- **Executive Dashboard (React)**: Sidebar controls, spotlight search, insights, and campaign priority table
- **FastAPI Service Layer**: Programmatic access to payload, KPIs, campaigns, quality checks

## Quick Start
### 1) Install
```powershell
pip install -r requirements.txt
```

### 2) Run Pipeline
```powershell
python -m src.main --run-date 2026-02-27
```

### 3) Launch Dashboard
```powershell
./run_frontend.ps1
```
Open: `http://localhost:5173`

### 4) Launch API
```powershell
./run_api.ps1
```
Open docs: `http://127.0.0.1:8000/docs`

### 5) One-Command Full Flow
```powershell
./run_consumer360.ps1 -RunDate 2026-02-27 -LaunchFrontend -LaunchApi
```

## API Endpoints
- `GET /health`
- `GET /payload`
- `GET /kpis`
- `GET /campaigns`
- `GET /quality`

## Output Artifacts
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
config/             Runtime and brand settings
docs/               Docs + visual assets
frontend/           React + Vite dashboard
reports/            Generated outputs
sql/                Schema and SQL scripts
src/                Analytics pipeline modules
```

## Roadmap
- Role-based auth and access control
- PDF executive report export
- Scenario simulator for campaign budget planning
- Docker + CI/CD deployment pipeline

## License
MIT
