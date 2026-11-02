# Civic Issue Reporter code

Run all application commands from this directory so Flask templates, static uploads, the SQLite instance directory and the Procfile keep their relative paths.

- app.py: Flask routes and local entry point.
- models/: SQLAlchemy entities.
- templates/ and static/: browser interface and assets.
- test-cases/: original example images; these are fixtures, not an automated test suite.
- instance/: local SQLite state, ignored by Git.

After installing requirements.txt, python app.py initializes a new local database and starts the development server. For a fresh WSGI deployment, initialize the schema before starting the existing gunicorn app:app command:

```sh
python -c "from app import app, db; app.app_context().push(); db.create_all()"
gunicorn app:app
```

Use code/ as the root for a GitHub-linked host, with pip install -r requirements.txt as the build step and the existing Procfile/start command. The repository reorganization does not deploy the application.

The current source is a prototype: it uses a fixed development session key, permits role selection during registration and starts its development server in debug mode. This folder-only change preserves application behavior; review those settings before accepting real users or data.
