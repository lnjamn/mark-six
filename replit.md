# Running on Replit

- This import retains its original Python/Flask structure and Flutter sources.
- Click **Run** to start the **Start application** workflow
  (`env -u DATABASE_URL python run.py`). This removes the environment-provided
  PostgreSQL URL only for the app process so the original SQLite default is used;
  it does not change or delete the environment variable or any external database.
- The Flask web app listens on `0.0.0.0:5000` and appears in Preview.
- Dependencies are listed in `requirements.txt`.
- Startup initializes the existing SQLite database at `data/lottery_system.db`.
  Runtime data is excluded from Git. No external database is required.
- Session signing uses `SECRET_KEY`, or Replit's existing `SESSION_SECRET`.
  Never commit either value.
- The first registered account becomes the administrator. Register your own account
  before sharing access to a fresh installation.
- AI features and email notifications require your own provider configuration in
  the admin panel; they are not needed to start the web app.
- The built-in scheduler uses Asia/Shanghai time. Set `ENABLE_SCHEDULER=0` to
  disable it if needed.
- This workflow is for workspace development, not a production deployment.
- The repository's noncommercial license still applies.
