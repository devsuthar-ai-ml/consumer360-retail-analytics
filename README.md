# Consumer360 - Production Retail Intelligence

Consumer360 is an end-to-end analytics product with automated pipeline, advanced React dashboard, and API layer.

## What is included
- SQL + Python analytics pipeline (RFM, Cohort, Market Basket, CLV)
- Data quality validation report on every run
- Advanced React command center UI (filters, spotlight, strategic insights, campaign priority)
- FastAPI service for payload/KPI/campaign integrations
- Weekly automation scripts

## Run pipeline
```powershell
pip install -r requirements.txt
python -m src.main --run-date 2026-02-27
```

## Run advanced frontend
```powershell
./run_frontend.ps1
```
Open: `http://localhost:5173`

## Run API
```powershell
./run_api.ps1
```
Open API docs: `http://127.0.0.1:8000/docs`

## Outputs
- `reports/data_quality_report.json`
- `reports/customer_rfm_segments.csv`
- `reports/customer_clv.csv`
- `reports/cohort_retention.csv`
- `reports/market_basket_rules.csv`
- `frontend/public/data/dashboard_payload.json`

## One-command full flow
```powershell
./run_consumer360.ps1 -RunDate 2026-02-27 -LaunchFrontend
```
