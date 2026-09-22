# Observability Stack Lab

This project is a small observability environment built with Prometheus, Grafana, Node Exporter and cAdvisor.

Prometheus collects metrics from the host and from running containers. Node Exporter is configured to read CPU, memory and filesystem data from the host VM, while cAdvisor provides container-level metrics.

Grafana is provisioned automatically when the stack starts. The Prometheus datasource, System Overview dashboard and CPU alert rule are all stored in the repository, so the environment can be recreated without configuring Grafana manually.

The dashboard includes CPU usage, memory usage, root filesystem usage and the number of active Prometheus targets.

A Grafana alert rule monitors host CPU usage and enters a pending state when usage is above 80%. It fires if that condition remains true for more than one minute.

The stack uses fixed image versions and persistent Docker volumes for Prometheus and Grafana data.

To run it:

cd monitoring
docker compose up -d

Services:

Grafana: http://localhost:3000
Prometheus: http://localhost:9090
cAdvisor: http://localhost:8080
Node Exporter: http://localhost:9100

The screenshots folder contains examples from previous validation of the monitoring stack and Grafana dashboards.
