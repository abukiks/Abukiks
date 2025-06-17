# ✅ TaskTrackr

A fully documented FastAPI-based microservice that follows the **12-Factor App Methodology**, built for DevOps learning and portfolio showcasing.

🔗 Live App: [https://tasktrackr.onrender.com](https://tasktrackr.onrender.com)  
🐳 Docker Image: [`yourusername/tasktrackr`](https://hub.docker.com/repository/docker/yourusername/tasktrackr)

---

## 📦 Tech Stack

- **FastAPI** – Web framework
- **SQLite / SQLAlchemy** – Database & ORM
- **Docker** – Containerization
- **GitHub Actions** – CI/CD
- **Render** – Cloud deployment
- **UptimeRobot** – Uptime monitoring
- **python-dotenv** – Config management

---

## 🚀 Features

- ✅ `/tasks` CRUD API
- ✅ `/health` endpoint for monitoring
- ✅ Environment-based config loading (`.env.dev`, `.env.prod`)
- ✅ Docker-ready & CI/CD pipeline with GitHub Actions
- ✅ One-off admin CLI commands (`admin.py`)

---

## 📘 12-Factor App Compliance

| #  | Factor                 | Applied? | Notes                                     |
|----|------------------------|----------|-------------------------------------------|
| 1️⃣ | **Codebase**          | ✅        | GitHub repo with main branch              |
| 2️⃣ | **Dependencies**      | ✅        | `requirements.txt` (or `poetry`) used     |
| 3️⃣ | **Config**            | ✅        | `.env` with `python-dotenv`               |
| 4️⃣ | **Backing Services**  | ✅        | Swappable DB via `DATABASE_URL`           |
| 5️⃣ | **Build, Release, Run**| ✅       | Docker handles build/release/run stages   |
| 6️⃣ | **Processes**         | ✅        | Stateless, self-contained FastAPI app     |
| 7️⃣ | **Port Binding**      | ✅        | `uvicorn` binds directly to port 8000     |
| 8️⃣ | **Concurrency**       | ✅        | Ready for multi-process container support |
| 9️⃣ | **Disposability**     | ✅        | Docker stop/start safe; CLI one-offs OK   |
| 🔟 | **Dev/Prod Parity**    | ✅        | `.env.dev` and `.env.prod` used           |
| 1️⃣1️⃣ | **Logs**           | ✅        | Logs to stdout with Python logging        |
| 1️⃣2️⃣ | **Admin Processes** | ✅        | `admin.py list/clean` as one-off commands |

---

## 🧑‍💻 Getting Started (Local)

```bash
git clone https://github.com/yourusername/tasktrackr.git
cd tasktrackr

# Setup
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Run
uvicorn main:app --reload
```

---

## 🐳 Docker Usage

```bash
# Build
docker build -t tasktrackr .

# Run
docker run -d -p 8000:8000 tasktrackr
```

---

## 🚀 Deployment (Render)

- Connect repo on [render.com](https://render.com/)
- Choose Docker environment
- Set environment variables:
  - `ENV=production`
  - `DATABASE_URL=sqlite+aiosqlite:///./tasks.db`

---

## 🛠 Admin Commands

```bash
python admin.py list     # Show all tasks
python admin.py clean    # Delete completed tasks
```

---

## 🔍 Monitoring

- `/health` endpoint added for status checks
- Registered with [UptimeRobot](https://uptimerobot.com)

---

## 🙌 Author

Built by **John Carl Abucay**  
📫 [abukiks.x@gmail.com](mailto:abukiks.x@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/yourprofile)

---

## 💡 Purpose

This project was built to **learn DevOps by doing** — every step from bootstrapping to production deployment follows **real industry standards**.
