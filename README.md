# Day 19 — Distributed Observability & Monitoring Platform

Java 17 + Spring Boot 3.3.5 project demonstrating centralized metrics, health checks and request tracing across services.

## Run
```bash
docker compose up --build
```

Services:
- Gateway: http://localhost:8080
- Metrics service: http://localhost:8081
- Prometheus: http://localhost:9090
- Grafana: http://localhost:3000

## API
```bash
curl http://localhost:8080/api/hello
curl http://localhost:8080/actuator/health
curl http://localhost:8081/actuator/prometheus
```

## GitHub
```bash
git init
git add .
git commit -m "Day 19 distributed observability platform"
git branch -M main
git remote add origin https://github.com/Vermaaditya3030/distributed-observability-day19.git
git push -u origin main
```
