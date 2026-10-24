# FastAPI Rate-Limiting Middleware

This repository contains test files and Docker configuration intended for a FastAPI backend project, but the current default-branch snapshot is incomplete: the application package imported by the tests (`src/`) is missing.

## Current status

- Pytest dependencies install successfully in GitHub Actions.
- The test run currently stops during test discovery with `ModuleNotFoundError: No module named 'src'`.
- The Dockerfile also expects `src/main.py`, which is not present in the current repository snapshot.

Because the application source is missing, the API and its tests cannot currently be verified from this repository alone.

## What is present

- Pytest test files and fixtures
- Requirements files
- Dockerfile and Docker Compose configuration
- Project notes and screenshots

## To restore a reproducible project

1. Restore the application package expected by the tests and Dockerfile.
2. Confirm the actual module layout and update imports only if the source structure is intentionally different.
3. Run `pytest -v` from a clean checkout.
4. Run `docker compose up --build` and verify the API health and database connection.
5. Replace the example database credentials in Docker Compose before using any shared environment.

The repository should not be presented as a currently runnable FastAPI service until the missing source has been restored and the tests pass.
