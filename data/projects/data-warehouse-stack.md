# Data Warehouse Stack

- Repo: github.com/Anhsnotes/data_warehouse (public, 12 stars, 7 forks)
- Languages: Python, Shell, Dockerfile, Open Policy Agent (Rego)
- Status: Active

## Description

A modern, lightweight, high-performance data analytics stack for medium-size teams. Deployable with a single command via Docker Compose. Includes an AI Analytics Assistant that converts natural language questions into SQL using OpenAI GPT-4.

## Tech Stack

- PostgreSQL (data warehouse)
- SQL Server (source: AdventureWorks)
- dbt Core (transformation layer)
- Apache Airflow (orchestration — implied by integration)
- Airbyte (EL via abctl)
- Streamlit (dashboards + AI assistant)
- OPA / OPAL (fine-grained access control with Rego policies)
- OpenAI GPT-4 (natural language to SQL)
- Docker Compose (full infrastructure)

## Key Capabilities Demonstrated

- End-to-end modern data stack architecture (EL + T + BI)
- AI-powered natural language analytics
- Role-based access control with OPA/OPAL (9 role types)
- Automated AI sync: dbt model changes auto-update LLM context and SQL validator
- Infrastructure-as-code with Docker Compose and shell scripts
- Git-based policy management
