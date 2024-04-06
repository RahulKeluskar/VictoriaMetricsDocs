# VictoriaMetrics vs Prometheus: System Properties Comparison

VictoriaMetrics is a monitoring system fully compatible with Prometheus, offering many of the same features along with additional benefits such as higher performance and scalability.

One key difference between VictoriaMetrics and Prometheus is VictoriaMetrics' inclusion of an anomaly detection feature. This feature helps identify unusual changes in metrics data, aiding in troubleshooting and problem identification.

Additional features of vmagent, compared to Prometheus:
- Lower resource requirements when scraping numerous targets or targets with a high number of exposed metrics.
- Independent disk-backed buffers for each configured remote storage, ensuring data delivery to healthy storage even if others are slow or temporarily unavailable.
- Support for multiple data ingestion protocols, enabling both pull and push models for data ingestion.

Prometheus lacks native High Availability, requiring duplication of instances for redundancy. VictoriaMetrics addresses the long-term storage limitation of Prometheus by providing a solution for extended retention and data durability.

