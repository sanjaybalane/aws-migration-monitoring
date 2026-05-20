# AWS Migration & Monitoring Prototype

## Overview

This project simulates a DevOps migration and observability workflow for an application moving towards an AWS / EC2 environment.

The application is containerized using Docker, automated using Ansible, and monitored through Prometheus, Grafana, and Node Exporter.

The goal is to demonstrate infrastructure automation, deployment reproducibility, monitoring, and operational visibility in a cloud-oriented environment.

---

## Tech Stack

### Infrastructure & Automation
- Docker
- Docker Compose
- Ansible

### Application
- Flask (Python)

### Monitoring & Observability
- Prometheus
- Grafana
- Node Exporter

### DevOps & Version Control
- Git
- GitHub

---

## Project Architecture

```txt
User
 ↓
Flask Application
 ↓
Docker Container
 ↓
Docker Compose Deployment
 ↓
Node Exporter Metrics
 ↓
Prometheus Metrics Collection
 ↓
Grafana Dashboards

Deployment automated using Ansible.
Simulated target environment: AWS EC2.
```

---

## Features

### Containerized Application Deployment

- Flask web application containerized using Docker
- Docker Compose orchestration
- Reproducible deployment workflow

### Deployment Automation

- Automated deployment execution using Ansible playbooks
- Infrastructure operations simplified through automation

### Monitoring & Observability

- System metrics collection using Node Exporter
- Prometheus metrics scraping and monitoring
- Grafana dashboards for infrastructure visualization

### Health Monitoring

Health endpoint implemented for service validation.

Endpoint:

```txt
/health
```

Response:

```json
{
  "status": "healthy"
}
```

---

## Project Structure

```txt
aws-migration-monitoring/
│
├── app/
│   ├── app.py
│   ├── Dockerfile
│   └── requirements.txt
│
├── ansible/
│   └── deploy.yml
│
├── monitoring/
│   └── prometheus.yml
│
├── docs/
│
├── docker-compose.yml
├── README.md
└── .gitignore
```

---

## Setup & Installation

### Clone Repository

```bash
git clone https://github.com/sanjaybalane/aws-migration-monitoring.git
cd aws-migration-monitoring
```

---

### Start Services

Run:

```bash
docker compose up -d --build
```

Check running containers:

```bash
docker ps
```

---

### Run Deployment Automation

Execute the Ansible playbook:

```bash
ansible-playbook ansible/deploy.yml
```

---

## Access Services

### Flask Application

```txt
http://localhost:5000
```

### Health Endpoint

```txt
http://localhost:5000/health
```

### Prometheus

```txt
http://localhost:9090
```

### Grafana

```txt
http://localhost:3000
```

Default login:

```txt
Username: admin
Password: admin
```

---

## Monitoring Configuration

### Prometheus

Configured to scrape:

- Node Exporter metrics
- Application metrics

Example validation query:

```txt
up
```

---

### Grafana Dashboard

Import dashboard:

```txt
Dashboard ID: 1860
```

(Node Exporter Full Dashboard)

Metrics visualized:

- CPU usage
- Memory usage
- Disk utilization
- Network activity
- System load

---

## Use Case

This project demonstrates:

- Containerization of applications
- Deployment automation
- Monitoring stack deployment
- Infrastructure observability
- DevOps operational workflow

It simulates a simplified migration and monitoring environment commonly used in AWS / Cloud / DevOps projects.

---

## Future Improvements

Potential enhancements:

- AWS EC2 deployment
- Terraform infrastructure provisioning
- Kubernetes orchestration
- Helm chart deployment
- GitHub Actions CI/CD pipeline
- CloudWatch integration
- IAM security hardening

---

## Author

**Sanjay Balane**

GitHub:  
https://github.com/sanjaybalane
