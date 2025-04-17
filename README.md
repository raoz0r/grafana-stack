# 📊 Grafana Monitoring Stack

A powerful, self-hosted Docker-based monitoring stack using **Grafana**, **Prometheus**, **cAdvisor**, **Node Exporter**, **Loki**, and **Promtail**.

## 🚀 Stack Overview

This stack provides:

- 🔍 System and container metrics with **Prometheus**, **Node Exporter**, and **cAdvisor**
- 📉 Beautiful dashboards via **Grafana**
- 📜 Log aggregation with **Loki** + **Promtail**

## 📦 Services

| Service        | Port  | Description                             |
|----------------|-------|-----------------------------------------|
| Grafana        | `3000`| Dashboard UI                            |
| Prometheus     | `9090`| Metrics scraping & querying             |
| cAdvisor       | `8080`| Container resource usage                |
| Node Exporter  | `9100`| System-level metrics                    |
| Loki           | `3100`| Log storage backend                     |
| Promtail       | `9080`| Log collection agent                    |

## 📁 Folder Structure

```
grafana-stack/
├── docker-compose.yml
├── prometheus.yml
├── loki-config.yaml
├── promtail-config.yaml
└── grafana/
    └── provisioning/
        └── datasources/
            └── ds-loki.yaml
```

## 🛠️ Requirements

- Docker
- Docker Compose
- Git
- Grafana account (optional, for dashboards sync)

## 🚀 Usage

1. Clone the repo:
    ```bash
    git clone git@github.com:raoz0r/grafana-stack.git
    cd grafana-stack
    ```

2. Launch the stack:
    ```bash
    docker compose up -d
    ```

3. Access services:
    - Grafana: http://localhost:3000 (default login: `admin` / `admin123`)
    - Prometheus: http://localhost:9090
    - cAdvisor: http://localhost:8080

## 📈 Dashboards

Use Grafana Dashboard ID `193` or create your own. Logs available via Loki → Explore tab.

## 📝 Credits
Built by [raoz0r](https://github.com/raoz0r)