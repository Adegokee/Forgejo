# Forgejo Git Hosting with Docker Compose (Production-Ready)

This project sets up Forgejo — a self-managed Git hosting solution — using Docker Compose.

---

## 📦 Features

- PostgreSQL database
- SMTP email support (for user registration, password reset, etc.)
- SSH access
- Persistent data and config volumes
- Health checks and auto-restart
- `.env` configuration

---

## 🚀 Setup

### 1. Clone the Repo

```bash
git clone https://git.edusuc.net/WEBFORX/infrastructure-tools.git
cd infrastructure-tools/forgejo
```

### 2. Configure Environment

Edit the `.env` file to match your environment and SMTP provider.

### 3. Run the Services

```bash
docker compose --env-file .env up -d
```

### 4. Access the App

- Web UI: [http://localhost:3000](http://localhost:3000)
- SSH: `ssh -p 2222 git@localhost`

---

## 📬 SMTP (Mail) Setup

Ensure you set these in `.env`:

- `FORGEJO_MAILER_HOST`
- `FORGEJO_MAILER_PORT`
- `FORGEJO_MAILER_USER`
- `FORGEJO_MAILER_PASSWORD`
- `FORGEJO_MAILER_FROM`

Example: Mailgun, Gmail, etc.

---

## 🗂️ Volumes

- Git repositories: `forgejo-data`
- Configuration: `forgejo-config`
- Database: `db-data`

---

## ✅ First-Time Setup

1. Open the UI in browser.
2. Complete the setup wizard.
3. Use your SMTP credentials for email-based notifications.
