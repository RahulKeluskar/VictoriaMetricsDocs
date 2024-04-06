# Cardinality of Metrics

Cardinality refers to the number of TimeSeries of a metric with single-valued labels. High cardinality metrics can pose challenges, particularly in Kubernetes clusters managing a large number of pods.

For instance, adding labels like pod_name or client_IP to a metric increases cardinality for each unique client call and pod. This increase in cardinality can strain systems like Prometheus, resulting in overconsumption of resources such as RAM.

Prometheus can perform poorly with multiple metrics exhibiting high cardinalities (> 100,000), potentially consuming significant amounts of RAM during high-load events.
