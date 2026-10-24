# FastAPI Rate-Limiting Middleware

A Python backend project built around a FastAPI service. The repository includes registration rate-limiting logic, authentication-related services, database integration, Docker configuration, and pytest tests.

## Included

- FastAPI application and API routes
- Rate limiting for registration
- Authentication and user-management services
- SQLAlchemy database integration
- Pytest tests for authentication, users, and todo services
- Dockerfile and Docker Compose configuration

## Run with Docker Compose

Requires Docker Engine or Docker Desktop with the Compose plugin.

```bash
docker compose up --build
```

The API is configured for port 8000. Stop the services with:

```bash
docker compose down
```

The Compose file uses example PostgreSQL credentials for local development only. Replace them and use environment-managed secrets before any shared or deployed environment.

## Run tests locally

Requires Python 3.11.

```bash
python -m venv .venv
# Windows PowerShell
.venv\Scripts\Activate.ps1
# macOS/Linux
source .venv/bin/activate

pip install -r requirements-dev.txt
pytest -v
```

## Continuous integration

GitHub Actions installs the development dependencies and runs pytest on pushes and pull requests targeting `main`. The result of each run is available in the repository's Actions tab.

## Notes

Run the tests and review the current dependency versions before relying on the project in another environment. This README does not imply a production deployment.
