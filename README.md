# ClimateMLAgents

Enterprise Multi-Agent Operational Intelligence Platform

AegisOps AI is a modular multi-agent AI platform designed to demonstrate modern AI Systems Engineering practices using:

- FastAPI
- LangGraph
- LangChain
- Tool-based architectures
- Governance and observability patterns
- Enterprise operational analytics

The platform simulates an enterprise operational intelligence system where AI agents analyze sales telemetry, detect anomalies, generate executive summaries, and orchestrate workflows using structured tool access.

---

# Project Goals

This project was created to demonstrate:

- Multi-agent orchestration
- Tool-use patterns
- AI governance
- Observability
- Operational intelligence
- Enterprise AI architecture
- FastAPI backend development
- LangGraph workflows
- Cloud-ready architecture

The system is intentionally designed with:
- minimal complexity,
- modular architecture,
- production-oriented engineering,
- and enterprise-ready patterns.

---

# Architecture Overview

```text
FastAPI
   ↓
LangGraph Orchestration
   ↓
Router Agent
   ↓
Specialized Agents
   ↓
Tool Layer
   ↓
Enterprise Data Sources
```

---

# Core Features

## Multi-Agent Workflows

The platform uses LangGraph to orchestrate specialized agents:

- Router Agent
- Analytics Agent
- Executive Agent
- Governance Agent

---

## Tool-Based Architecture

Agents never access data sources directly.

All external interactions happen through tools:

- Sales Tool
- Telemetry Tool
- Governance Tool
- Analytics Tool

This architecture follows modern MCP-style patterns for governed AI access.

---

## Governance & Security

The platform includes:
- Prompt injection detection
- SQL validation
- Audit logging
- Tool governance
- Structured tracing

---

## Operational Intelligence

The system analyzes:
- sales performance,
- operational anomalies,
- telemetry,
- governance events,
- and executive KPIs.

---

# Tech Stack

| Component | Technology |
|---|---|
| API Framework | FastAPI |
| Orchestration | LangGraph |
| Agent Framework | LangChain |
| Data Processing | Pandas |
| Validation | Pydantic |
| Runtime | Python 3.12+ |
| Deployment | Docker |
| Cloud Target | AWS |

---

# Project Structure

```text
aegisops-ai/
│
├── app/
│   ├── api/
│   ├── agents/
│   ├── orchestration/
│   ├── tools/
│   ├── governance/
│   ├── observability/
│   ├── schemas/
│   ├── core/
│   └── main.py
│
├── data/
│   └── sales/
│
├── tests/
│
├── docs/
│
├── scripts/
│
├── docker/
│
├── infrastructure/
│
├── .cursor/
│
├── .env.example
├── .gitignore
├── docker-compose.yml
├── requirements.txt
└── README.md
```

---

# Dataset

The project uses the Superstore Dataset for:
- sales analytics,
- anomaly detection,
- executive reporting,
- operational intelligence workflows.

Dataset location:

```text
data/sales/superstore.csv
```

---

# Local Development Setup

## 1. Clone repository

```bash
git clone <repository-url>
cd aegisops-ai
```

---

## 2. Create virtual environment

### Linux / Mac

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### Windows

```bash
python -m venv .venv
.venv\Scripts\activate
```

---

## 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 4. Configure environment

Create:

```text
.env
```

Example:

```env
APP_ENV=development
LOG_LEVEL=INFO
```

---

## 5. Run application

```bash
uvicorn app.main:app --reload
```

---

## 6. Open API Docs

```text
http://127.0.0.1:8000/docs
```

---

# Example Queries

## Sales Analytics

```text
Show regions with declining profits.
```

---

## Operational Intelligence

```text
Detect abnormal sales behavior.
```

---

## Executive Reporting

```text
Generate an executive sales summary.
```

---

## Governance

```text
Were any suspicious operational events detected?
```

---

# Development Principles

The platform follows:

- simplicity-first engineering,
- low-complexity architecture,
- minimal abstractions,
- explicit workflows,
- production-oriented patterns.

The project intentionally avoids:
- overengineering,
- excessive microservices,
- unnecessary enterprise boilerplate,
- speculative abstractions.

---

# Security Principles

- Agents never access databases directly
- All external access happens through tools
- Prompt injection detection is enforced
- SQL validation is mandatory
- Audit logging is enabled
- Environment variables are required for secrets

---

# Deployment Roadmap

## Phase 1
- Local FastAPI platform
- Mock tools
- LangGraph orchestration

## Phase 2
- Governance layer
- Observability
- Structured tracing

## Phase 3
- Docker deployment
- AWS readiness

## Phase 4
- Bedrock integration
- OpenSearch integration
- Snowflake integration

---

# Future Enhancements

- AWS Bedrock integration
- OpenSearch retrieval
- Vector search
- Real-time telemetry
- Advanced governance
- Agent evaluation pipelines
- Multi-tenant orchestration

---

# Design Philosophy

Enterprise-quality AI systems with startup-level simplicity.