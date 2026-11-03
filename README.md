# FinSight

FinSight is a portfolio analytics prototype built for the Design Experience course. This repository contains the Python backend. It accepts portfolio holdings and optional transaction history as CSV files, calculates performance and allocation, measures concentration and diversification, and combines available signals into a rule-based Portfolio Health Score.

## Run locally

Use Python 3.10 or newer. From the repository root, run:

```sh
python -m venv .venv
```

Activate the environment using `.venv\Scripts\Activate.ps1` on Windows PowerShell or `source .venv/bin/activate` on macOS or Linux, then run:

```sh
python -m pip install -r requirements.txt
python -m uvicorn backend.main:app
```

Open http://127.0.0.1:8000/docs for the interactive API documentation. Try the bundled CSVs in `data/`. The app initializes its own SQLite database locally.

```sh
python -m pytest
```

## Scope of this snapshot

This snapshot includes FastAPI endpoints, SQLite storage, analytics, risk and diversification, transaction behaviour analysis, and the Health Score. The dashboard design and the AI engine described in the team reports are outside this snapshot. The insights endpoint is a placeholder. The API is intended for local academic demonstration with sample data.

See [API notes](docs/api.md) and the methodology files in [docs](docs/).

## Team

- Ricky Maishari — frontend and dashboard design, testing contributions
- Jash Vora — backend and API integration
- Aditya Shah — portfolio analytics
- Soumil Patro — risk and diversification
- Prisha Mistry — behaviour analysis
- Rayyan Chunawala — AI insights
- Atharva Suryavanshi — sample data, testing, and integration

[MIT License](LICENSE)
