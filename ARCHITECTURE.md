# Architecture
Client -> Gateway -> Metrics Service
                     |-> Actuator metrics
Prometheus scrapes both services; Grafana visualizes Prometheus data.
