# Prometheus Architecture
![img](./img/k8s_prometheus_architecture.jpg)
Prometheus scraps metrics from instrumented jobs either directly or via an intermediary push gateway for short-lived jobs.

## Client Library
![img](./img/k8s_prometheus_client_libs.jpg)
Before you can monitoring your services, you need to add instrumentation to their code via one of the Prometheus client libraries:
- The client library sits in the application. 
- The client library go and gather the metrics on your application and format them to what prometheus can understand

## Exporters
![img](./img/k8s_prometheus_exporters.jpg)
We use exporters to instrument applications which we don't have the source code for, such as:
- Database
- Hardware
- Issue tracker and CI
- Messaging
- Storage
- HTTP
- API
- Logging

For more details: [EXPORTERS AND INTEGRATIONS](https://prometheus.io/docs/instrumenting/exporters/)

## Service Discovery
![img](./img/k8s_prometheus_service_discovery.jpg)
How does prometheus access to the metrics of the application? we can 
* define the target in prometheus configuration
* use service discovery

## Reference
[How to Setup Prometheus Monitoring On Kubernetes Cluster](https://devopscube.com/setup-prometheus-monitoring-on-kubernetes/)
