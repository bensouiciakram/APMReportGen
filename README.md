# APMReportGen

APMReportGen is a distributed FastAPI + Celery application designed to process large volumes of web application log data and generate detailed Application Performance Monitoring (APM) reports. The system ingests raw logs, aggregates performance metrics (latency percentiles, throughput, error rates), and produces a structured PDF report.

## 🚀 Features

- FastAPI-based API for log ingestion and report retrieval  
- Celery worker for heavy data processing and PDF generation  
- Redis as the message broker and Celery backend  
- Clean modular architecture (API layer, task layer, aggregation layer)  
- Supports CSV/JSON log ingestion  
- Generates APM PDF reports using templates  
- Fully containerized using Docker & docker-compose  

## 📂 Project Structure (Simplified)
apm_report_gen/
├── apm_report_gen/
│ ├── api/ # FastAPI routers
│ ├── tasks/ # Celery tasks (ingestion, aggregation, reporting)
│ ├── core/ # Business logic (aggregator, preprocessor, PDF utilities)
│ ├── models/ # Pydantic models
│ ├── templates/ # PDF report templates
│ └── celery_app.py # Celery initialization
├── docker-compose.yml
├── Dockerfile.api
├── Dockerfile.worker
└── README.md


## 🧰 Tech Stack

- **FastAPI** — Web framework  
- **Celery** — Distributed task queue  
- **Redis** — Broker & backend  
- **Python 3.10+**  
- **Docker & docker-compose**  
- **Jinja2 + WeasyPrint/ReportLab** for PDF generation  

## 🏗️ Running the Project (Coming Soon)

Setup and run instructions will be added as development progresses.

## 📌 Roadmap

- [ ] Implement log ingestion endpoint  
- [ ] Build Celery ingestion + aggregation tasks  
- [ ] Add PDF report generation  
- [ ] Add API endpoint for downloading reports  
- [ ] Add test suite (unit + integration)  

## 📄 License

MIT License

---

> ⚠️ *This project is currently under active development. More documentation will be added soon.*
