# Analytics App Framework

- Repo: github.com/Anhsnotes/analytics_app_framework (private)
- Languages: Python, JavaScript, Dockerfile, Shell, HTML, CSS
- Status: Active

## Description

A modular, multi-stack platform for construction project management and data analytics. Combines a React + FastAPI web app, Apache Airflow for data orchestration with Kafka integration, and centralized logging with Loki + Grafana.

## Tech Stack

- React + Vite (frontend)
- FastAPI (backend API)
- PostgreSQL (application database)
- Apache Airflow with CeleryExecutor + Redis (data orchestration)
- Kafka (event streaming — consumers, producers, filters)
- MinIO (S3-compatible object storage)
- Loki + Promtail + Grafana (centralized logging and monitoring)
- Docker Compose (multi-stack deployment)

## Key Capabilities Demonstrated

- Full-stack web application development (React + FastAPI)
- Event-driven data pipelines with Kafka
- Airflow DAG authoring (user analytics, product events pipelines)
- Centralized log aggregation and observability (Loki/Grafana)
- Cross-stack Docker networking
- Construction domain: project hierarchy, milestones, progress tracking
