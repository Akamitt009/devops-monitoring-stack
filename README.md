# 🚀 Monitoring & Observability Stack using Prometheus, Grafana, Node Exporter, cAdvisor & NGINX

A complete real-time monitoring and observability setup built using Prometheus, Grafana, Node Exporter, cAdvisor, Docker, and NGINX on an Azure Linux VM.

This project demonstrates infrastructure monitoring, container monitoring, system metrics collection, dashboard visualization, and web server monitoring using modern DevOps tools.

---

# 📌 Project Overview

This monitoring stack collects and visualizes:

- ✅ Server CPU Usage
- ✅ Memory Usage
- ✅ Disk Utilization
- ✅ Network Traffic
- ✅ Docker Container Metrics
- ✅ NGINX Monitoring
- ✅ Real-time Infrastructure Metrics
- ✅ Prometheus Targets Health
- ✅ Grafana Dashboards

---

# 🛠️ Tech Stack

| Tool | Purpose |
|------|----------|
| Prometheus | Metrics Collection |
| Grafana | Visualization Dashboard |
| Node Exporter | Linux System Metrics |
| cAdvisor | Docker Container Monitoring |
| Docker | Container Runtime |
| NGINX | Web Server Monitoring |
| Azure VM | Hosting Environment |

---

# ☁️ Azure Infrastructure

- Azure Linux Virtual Machine
- Ubuntu Server
- Docker Installed
- Public IP Enabled
- Monitoring Ports Exposed

---

# 📂 Project Architecture

```text
Node Exporter ---> Prometheus ---> Grafana
cAdvisor -------> Prometheus ---> Grafana
NGINX ----------> Prometheus ---> Grafana
```

---

# ⚙️ Components Configured

## 🔹 Node Exporter

Used for collecting:

- CPU Metrics
- RAM Metrics
- Disk Usage
- Network Statistics
- System Load

Metrics Endpoint:

```bash
http://<SERVER-IP>:9100/metrics
```

---

## 🔹 Prometheus

Configured Prometheus to scrape metrics from:

- Node Exporter
- cAdvisor

Prometheus Targets Page:

```bash
http://<SERVER-IP>:9090/targets
```

---

## 🔹 Grafana

Integrated Grafana with Prometheus datasource and imported dashboards for visualization.

Dashboard Features:

- CPU Monitoring
- Memory Monitoring
- Disk Monitoring
- Network Monitoring
- Container Metrics

Grafana URL:

```bash
http://<SERVER-IP>:3000
```

---

## 🔹 cAdvisor

Used for Docker container monitoring.

Collected:

- Container CPU Usage
- Container RAM Usage
- Container Network Usage
- Docker Container Statistics

cAdvisor URL:

```bash
http://<SERVER-IP>:8081
```

---

## 🔹 NGINX Monitoring

Configured NGINX stub_status module for monitoring.

NGINX Metrics URL:

```bash
http://<SERVER-IP>:8080/stub_status
```

---

# 📸 Project Screenshots

## 🔹 Node Exporter Metrics Endpoint

![Node Exporter Metrics](screenshots/node-exporter-metrics.png)

---

## 🔹 Prometheus Targets Dashboard

![Prometheus Targets](screenshots/prometheus-targets.png)

---

## 🔹 Grafana Node Exporter Dashboard

![Grafana Dashboard](screenshots/grafana-node-exporter-dashboard.png)

---

## 🔹 NGINX Stub Status Monitoring

![NGINX Monitoring](screenshots/nginx-stub-status.png)

---

## 🔹 cAdvisor Container Monitoring

![cAdvisor](screenshots/cadvisor-container-monitoring.png)

---

# 🐳 Docker Containers Used

| Container | Purpose |
|-----------|----------|
| Prometheus | Metrics Collection |
| Grafana | Dashboard Visualization |
| cAdvisor | Container Monitoring |
| NGINX | Web Server |
| Node Exporter | System Monitoring |

---

# 📁 Project Structure

```text
monitoring-observability-stack/
│
├── screenshots/
│   ├── node-exporter-metrics.png
│   ├── prometheus-targets.png
│   ├── grafana-node-exporter-dashboard.png
│   ├── nginx-stub-status.png
│   └── cadvisor-container-monitoring.png
│
├── prometheus.yml
├── docker-compose.yml
├── README.md
└── dashboards/
```

---

# ⚡ Prometheus Configuration

```yaml
global:
  scrape_interval: 15s

scrape_configs:
  - job_name: 'node_exporter'
    static_configs:
      - targets: ['localhost:9100']

  - job_name: 'cadvisor'
    static_configs:
      - targets: ['localhost:8081']
```

---

# 🚀 How to Run the Project

## 1️⃣ Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/monitoring-observability-stack.git
```

---

## 2️⃣ Move into Project Directory

```bash
cd monitoring-observability-stack
```

---

## 3️⃣ Start Containers

```bash
docker compose up -d
```

---

## 4️⃣ Verify Running Containers

```bash
docker ps
```

---

# 🌐 Service Ports

| Service | Port |
|---------|------|
| Grafana | 3000 |
| Prometheus | 9090 |
| Node Exporter | 9100 |
| cAdvisor | 8081 |
| NGINX | 8080 |

---

# 📊 Monitoring Features Implemented

- Real-time Infrastructure Monitoring
- Docker Container Monitoring
- Prometheus Metrics Collection
- Grafana Visualization
- NGINX Status Monitoring
- Azure VM Monitoring
- Linux Server Observability

---

# 🔥 Key Learnings

- Prometheus Metrics Scraping
- Grafana Dashboard Management
- Docker Monitoring
- Linux System Monitoring
- Observability Concepts
- NGINX Metrics Collection
- Azure VM Deployment
- Infrastructure Monitoring

---

# 🎯 Future Improvements

- AlertManager Integration
- Loki Log Monitoring
- Promtail Log Collection
- Kubernetes Monitoring
- Slack Alerts
- Email Notifications

---

# 👨‍💻 Author

Amit Kumar

---

# ⭐ If you found this project useful, give it a star on GitHub!
