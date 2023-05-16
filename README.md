# kube-monitor
How to monitor pods //checks

NodeMetrics - 
#kubectl apply -f node-exporter.yml
#kubectl apply -f node-exporter-service.yml
#kubectl port-forward --address localhost,<pvt.ip> service/node-exporter 9100:9100

Kube-metrics -
#git clone https://github.com/kubernetes/kube-state-metrics  (also in this repo)
#kubectl apply -f kube-state-metrics/examples/standard/
#kubectl port-forward --address localhost,<pvt.ip> svc/kube-state-metrics -n kube-system 8080:8080

---------------------------------------------
Prometheus -

Create prometheus.yml. (Sample file in this repo)
#docker run -d -p 172.31.23.75:9090:9090 -v $<path>/prometheus.yml:/etc/prometheus/prometheus.yml prom/prometheus

---------------------------------------------

Grafana - pending


