# VictoriaMetrics Cluster Architecture

VictoriaMetrics can be deployed as a single server or as a cluster version, with the cluster version being preferred for scalability and performance. The cluster components include:

- vmstorage: Stores raw data and serves queried data for given time ranges and label filters.
- vminsert: Accepts ingested data and spreads it among vmstorage nodes based on consistent hashing over metric name and labels.
- vmselect: Performs incoming queries by fetching required data from all configured vmstorage nodes.
- vmauth: A simple auth proxy and router for the cluster, supporting various authentication methods.
- vmagent: Collects metrics from various sources and stores them in VictoriaMetrics or other Prometheus-compatible storage systems.
- vmalert: Executes alerting or recording rules against configured data sources and sends notifications using Alertmanager.
- promxy: A Prometheus proxy for querying data from multiple clusters.

Cluster resizing and scalability can be achieved through vertical and horizontal scaling of components, with vmstorage being the only stateful component.

