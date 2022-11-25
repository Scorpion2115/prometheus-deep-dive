# Application Monitoring
## Instrumenting Application
1. Deploy a sample application written by Node.js
```bash
# Build the image
sudo docker build -t evan21/swagger-test .

# Run the image
sudo docker run -p 3000:3000 -d evan21/swagger-test

# Optional Push the image to Dockerhub
sudo docker login --username=evan21
sudo docker push evan21/swagger-test
```

2. Generate some traffic to the application's URL
```bash
http://<ip-address>:3000/

# go to swagger stats ui
http://<ip-address>:3000/swagger-stats/ui

# browse swagger stats metrics which can be pasted in prometheus
http://<ip-address>:3000/swagger-stats/metrics
```

## Collecting Metrics from Applications

## Reference
[CLIENT LIBRARIES](https://prometheus.io/docs/instrumenting/clientlibs/)
