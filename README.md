# FastAPI Rate-Limiting Middleware

A Python backend project built around a FastAPI service, with rate limiting applied to registration and a test suite using pytest. The repository includes Docker configuration and dependencies for local development.

## What is included

- FastAPI application structure
- Registration rate-limiting logic
- Authentication-related service code
- PostgreSQL-backed configuration, with SQLite described as a local alternative in the project setup
- Pytest tests for authentication, users, and todo services
- Docker Compose configuration

## Run with Docker

1. Install Docker Desktop or Docker Engine with the Compose plugin.
2. From the repository root, run:

   ```bash
   docker compose up --build
   ```

3. Stop the services with:

   ```bash
   docker compose down
   ```

## Run locally

Create and activate a virtual environment, then install the development dependencies:

```bash
python -m venv .venv
# Windows PowerShell:
.venv\Scripts\Activate.ps1
# macOS/Linux:
source .venv/bin/activate

pip install -r requirements-dev.txt
```

The original project instructions refer to the application entry point `src.main:app`. If the local source layout differs, use the actual module path in the repository.

## Run tests

```bash
pytest
```

## Technology

Python, FastAPI, pytest, Docker, Docker Compose, and database integration.

The repository's tests and deployment configuration should be run locally to confirm their current status; this README does not imply that a CI run has passed.
