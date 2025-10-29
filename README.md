# ConfigMonitoringDemo
<img width="1389" height="862" alt="image" src="https://github.com/user-attachments/assets/d7f996f0-38c5-4f83-88d5-44ee2430d0e9" />

<img width="1855" height="867" alt="image" src="https://github.com/user-attachments/assets/c7af7c8a-d0a7-4908-b8aa-3dae960d8219" />

# ConfigMonitoringDemo

## Overview
This repository serves as a documentation and integration reference for:
- The **OrderServiceDemo (.NET 8 + Steeltoe)** microservice
- The **ConfigServerDemo (Spring Boot + Spring Cloud Config Server)** configuration server
- The **Monitoring setup (Prometheus + Grafana)**

It demonstrates how configuration and monitoring are integrated across microservices using both .NET and Java-based tools.

---

## Architecture
OrderServiceDemo (.NET)
|
|--- Connects to ---> ConfigServerDemo (Spring Boot)
|
|--- Exposes metrics to ---> Prometheus
|
|--- Visualized in ---> Grafana

yaml
Copy code

---

## Repository Links
- **Order Service (.NET)** → [OrderServiceDemo](https://github.com/anubhd2/OrderServiceDemo)
- **Config Server (Spring Boot)** → [ConfigServerDemo](https://github.com/anubhd2/ConfigServerDemo)

---

## Setup Instructions (Placeholder)

### 1. Prerequisites
- Docker Desktop installed and running
- .NET 8 SDK
- Java 21 SDK
- Maven 3.9+
- Prometheus and Grafana Docker images pulled locally

### 2. Start Config Server
```bash
cd ConfigServerDemo
mvn spring-boot:run
3. Run Order Service
bash
Copy code
cd OrderServiceDemo
dotnet run
4. Start Prometheus
bash
Copy code
docker run -d -p 9090:9090 -v <path_to_prometheus.yml>:/etc/prometheus/prometheus.yml prom/prometheus
5. Access Grafana
bash
Copy code
http://localhost:3000
Dashboard and Metrics (Placeholder)
Screenshots and query examples will be added here:

process_cpu_seconds_total

microsoft_aspnetcore_hosting_http_server_request_duration

Custom metrics visualization in Grafana

Folder Structure
arduino
Copy code
ConfigMonitoringDemo/
│
├── README.md
├── screenshots/
│   ├── prometheus_dashboard.png
│   ├── grafana_dashboard.png
│
└── docs/
    ├── architecture-diagram.png
    └── setup-guide.md
Future Enhancements
Add alerting rules for Prometheus

Automate setup using Docker Compose

Introduce tracing via OpenTelemetry
