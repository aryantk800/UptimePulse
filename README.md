# ⏱️ UptimePulse – Website Monitoring Platform

UptimePulse is a lightweight website monitoring tool that regularly checks the health of user-defined URLs and reports their uptime status. Built with a modern DevOps pipeline, it features containerized deployment, CI/CD automation, and real-time monitoring dashboards.

---

## 🚀 Features

- Add/remove URLs to monitor
- Periodic uptime & latency checks
- Backend API built with Node.js
- React frontend dashboard
- Dockerized microservices architecture
- Kubernetes deployment with Helm support
- CI/CD via GitHub Actions
- Monitoring with Prometheus & Grafana

---

## 🛠️ Tech Stack

| Layer            | Tools & Frameworks                            |
|------------------|-----------------------------------------------|
| Frontend         | React, Tailwind CSS                           |
| Backend          | Node.js, Express                              |
| Worker           | Node.js (uptime checker using cron/interval) |
| Containerization | Docker, Docker Compose                        |
| IaC              | Terraform                                     |
| Orchestration    | Kubernetes (Minikube/GKE)                     |
| CI/CD            | GitHub Actions                                |
| Monitoring       | Prometheus, Grafana                           |
| Secrets          | GitHub Secrets, K8s Secrets                   |

---

## 📦 Project Structure

```text
UptimePulse/
├── client/                         # React frontend
│   ├── public/
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── App.jsx
│       └── index.js
│   ├── Dockerfile
│   └── package.json
│
├── server/                         # Node.js backend API
│   ├── routes/
│   ├── controllers/
│   ├── models/
│   ├── services/
│   ├── app.js
│   ├── Dockerfile
│   └── package.json
│
├── worker/                         # Uptime checker service
│   ├── index.js
│   ├── metrics.js
│   ├── scheduler.js
│   ├── Dockerfile
│   └── package.json
│
├── infra/                          # Terraform IaC files
│   ├── main.tf
│   ├── variables.tf
│   └── outputs.tf
│
├── k8s/                            # Kubernetes manifests
│   ├── client-deployment.yaml
│   ├── server-deployment.yaml
│   ├── worker-deployment.yaml
│   ├── ingress.yaml
│   └── service-monitor.yaml
│
├── monitoring/                     # Prometheus & Grafana setup
│   ├── prometheus.yml
│   └── grafana-dashboard.json
│
├── .github/                        # GitHub Actions workflows
│   └── workflows/
│       └── ci-cd.yml
│
├── docker-compose.yml             # Multi-container dev setup
├── README.md
├── LICENSE
└── .gitignore
```

⚙️ Getting Started
1. Clone the Repository
   git clone https://github.com/YOUR_USERNAME/UptimePulse.git
   cd UptimePulse

2. Run Services Locally
   Frontend
   cd client
   npm install
   npm start

   Backend
   cd ../server
   npm install
   npm run dev

   Worker
   cd ../worker
   npm install
   node index.js

3. Using Docker Compose
   To run all services together for development:
   docker-compose up --build

☸️ Deployment
Kubernetes: Use the manifests in the /k8s/ directory to deploy to a cluster like Minikube or GKE.
Terraform: Use the configuration files in /infra/ to provision infrastructure on cloud providers like AWS or GCP.

📊 Monitoring
Prometheus scrapes uptime and latency metrics from the backend and worker.
Grafana visualizes the metrics using the pre-configured dashboard (monitoring/grafana-dashboard.json).
