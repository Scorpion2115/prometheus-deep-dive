# README
Prometheus server uses a `pull method` to collect metrics.

Pushgateway serves as a middle-man for some use cases where a `push method` is necessary, such as monitoring a short live batch job processes.
- Client push metrics data to Pushgateway
- Prometheus server pulls metrics from the Pushgateway, just like any other exporter.

Define a Pushgateway job
```yml
 scrape_configs:
      - job_name: 'Pushgateway'
        # allow the metrics provider to supply their job names and instance names
        honor_labels: true
        static_configs:
        # by default, the pushgateway resides on port 9091
        - targets: ['<host-ip>:9091']
```

