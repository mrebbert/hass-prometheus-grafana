# HomeAssistant-prometheus-grafana
Little docker-compose setup to combine HomeAssistant with Prometheus and Grafana.

##Prerequisites
### Docker 
Update your docker installation to the newest version and install docker-compose if not already happened.

### HomeAssistant
Add
 
```
#Example configuration.yaml entry
prometheus:
```
to your `configuration.yaml` and restart your instance.

### This setup
Change `prometheus/prometheus.yml` to your needs. In minimum change the API password and the Hostname/IP to your settings.
Edit `config.monitoring` to change the password of the grafana admin.

### Startup
```
docker-compose up
```
starts two containers: Prometheus and Grafana.
Prometheus listens on Port 9090 and Grafana on 3000.
