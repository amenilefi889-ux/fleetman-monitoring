# fleetman-monitoring

Prometheus + Grafana pour le cluster minikube fleetman.

## Installation
kubectl create namespace monitoring
helm install prometheus prometheus-community/prometheus -n monitoring -f monitoring/prometheus-values.yaml
helm install grafana grafana/grafana -n monitoring -f monitoring/grafana-values.yaml

## Dashboard
Grafana > Dashboards > New > Import > Upload JSON : monitoring/fleetman-dashboard.json
(choisir Prometheus comme source de données si demandé)
