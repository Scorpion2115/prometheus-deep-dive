# Application Monitoring
## Collecting Metrics from Applications
1. Deploy a sample application written by Node.js

2. Generate some traffic to the application's URL
```bash
http://10.223.90.111:30081/

# go to swagger stats ui
http://10.223.90.111:30081/swagger-stats/ui

# browse swagger stats metrics which can be pasted in prometheus
http://10.223.90.111:30081/swagger-stats/metrics
```

## Reference
[CLIENT LIBRARIES](https://prometheus.io/docs/instrumenting/clientlibs/)