# VictoriaMetrics Stack Helm Chart Installation

To install the VictoriaMetrics Stack using Helm charts, follow these steps:

1. Add repositories for dependencies:
```bash
$ helm repo add grafana https://grafana.github.io/helm-charts
$ helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
```

2. Add the VictoriaMetrics repository and update:
```bash
$ helm repo add vm https://victoriametrics.github.io/helm-charts/
$ helm repo update
```

3. Retrieve default configuration values:
```bash
$ helm show values vm/victoria-metrics-k8s-stack > default-values.yaml
```

4. Customize the configuration values in `default-values.yaml` as needed.

5. Deploy the stack to a new namespace:
```bash
$ helm upgrade --install victoria-metrics-k8s-stack -n monitoring --create-namespace vm/victoria-metrics-k8s-stack -f monitoring-values.yaml
```

6. Verify the deployment by checking the pods and application status


