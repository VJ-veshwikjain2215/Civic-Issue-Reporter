# Civic Issue Reporter

A Flask prototype for reporting local civic issues, viewing reports, and managing officer and administrator dashboards. Image classification is currently a mock service.

## Repository structure

- [code/](code/README.md): Flask application, models, templates, static assets, deployment Procfile and sample images.
- [documents/](documents/README.md): setup, structure and planning notes.
- .github/: repository verification workflow.

## Run locally

Use Python 3.11+ and a virtual environment. From the repository root:

```sh
cd code
python -m venv .venv
# Activate .venv for your shell, then:
python -m pip install -r requirements.txt
python app.py
```

The development application creates its SQLite schema and listens on port 5000. Existing local database contents are preserved in code/instance/ and excluded from Git. Fresh clones create a new database; no existing account or report data is distributed.

For deployment setup and current prototype limitations, see [code setup](code/README.md).
