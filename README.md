# Observability Lab

Third project in a series focused on building a complete DevOps pipeline. The first two projects covered infrastructure provisioning and CI/CD automation. This one closes the cycle by adding visibility into what's actually running.

## What it does

Collects metrics from the VM and containers, stores them in Prometheus, and visualizes everything in Grafana. Also includes an alert rule that fires when CPU usage exceeds 80% for more than a minute.

## Stack

- **Prometheus** — scrapes and stores metrics
- **Grafana** — dashboards and alert rules
- **Node Exporter** — exposes VM-level metrics (CPU, RAM, disk)
- **cAdvisor** — exposes container-level metrics

## Running locally

```bash
cd monitoring
docker compose up -d
```

Grafana runs on port 3000, Prometheus on 9090, cAdvisor on 8080.

## Related projects

- [Project 1 — nginx-multisite-lab](https://github.com/Gabrieldelacerda/nginx-multisite-lab)
- [Project 2 — cicd-pipeline-aws](https://github.com/Gabrieldelacerda/cicd-pipeline-aws)
