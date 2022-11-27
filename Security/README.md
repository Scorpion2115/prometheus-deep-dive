# README
Prometheus does not provide authentication out of the box
![img](./img/unsecure.jpg)
You need to add your own security layer on top of the prometheus server:
- Basic Auth
- Reserver Proxy (Apache, Nginx)
![img](./img/reserve-proxy.jpg)