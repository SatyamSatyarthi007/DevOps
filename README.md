<div align="center">

# 🚀 Two-Tier Web App

**A production-ready, containerized full-stack app — built with Flask, PostgreSQL, Docker & Jenkins.**

![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-2.3-000000?style=flat-square&logo=flask&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?style=flat-square&logo=docker&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-CI%2FCD-D24939?style=flat-square&logo=jenkins&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-EC2-FF9900?style=flat-square&logo=amazonaws&logoColor=white)

</div>

---

## ✨ About

A two-tier web application with a **GlassOS** glassmorphism UI — dark-mode dashboard with animated mesh background, responsive sidebar, live notification panel, and real-time service health monitoring.

Built as a complete DevOps project covering containerization, CI/CD automation, and cloud deployment on AWS EC2.

---

## 🏗️ Architecture

```
GitHub → Jenkins (clone → build → deploy) → Docker Compose → Flask :5000 + PostgreSQL :5432
```

---

## 🚀 Quick Start

```bash
git clone https://github.com/SatyamSatyarthi007/DevOps.git
cd DevOps/two-tier-app
docker-compose up --build
```

Open [http://localhost:5000](http://localhost:5000) in your browser.

---

## 📁 Project Structure

```
two-tier-app/
├── frontend/
│   ├── app.py                  # Flask app — routes, auth, DB logic
│   ├── requirements.txt        # Python dependencies
│   ├── dockerfile              # Container definition
│   └── templates/
│       ├── login.html          # GlassOS sign in page
│       ├── register.html       # Account creation page
│       └── dashboard.html      # GlassOS dashboard
├── docker-compose.yml          # Orchestrates web + db services
├── jenkinsfile                 # CI/CD pipeline (3 stages)
└── README.md
```

---

## 🔧 Environment Variables

| Variable | Default | Description |
|---|---|---|
| `DB_HOST` | `db` | PostgreSQL host (Docker service name) |
| `DB_NAME` | `flask_db` | Database name |
| `DB_USER` | `myuser` | Database user |
| `DB_PASSWORD` | `mypassword` | Database password |
| `SECRET_KEY` | `supersecretkey` | Flask session secret |

---

## 🎨 UI Features

- Glassmorphism design with animated mesh background and floating orbs
- GlassOS dashboard — sidebar navigation, stat cards, pod timeline chart
- Live notification bell with unread count and per-notification read state
- Responsive — mobile hamburger menu, adaptive grid layouts
- Sections: Dashboard, Monitoring, Deployments, Infrastructure, Settings

---

## 🔄 CI/CD Pipeline (Jenkins)

```
Stage 1: Clone   →  Pull latest code from GitHub (main branch)
Stage 2: Build   →  docker-compose build
Stage 3: Deploy  →  docker-compose down && docker-compose up -d
```

Jenkins runs on AWS EC2 (`c7i-flex.large`) and auto-deploys on every push.

---

## 🔐 Auth

- SHA-256 password hashing
- Flask session-based login
- PostgreSQL `users` table auto-created on first run via `init_db()`

---

<div align="center">
Made with ❤️ using Flask · PostgreSQL · Docker · Jenkins · AWS EC2
</div>
