# Basado en Prometheus
FROM prom/prometheus

# Instalamos Grafana
RUN apt-get update && apt-get install -y wget software-properties-common
RUN wget -q -O - https://packages.grafana.com/gpg.key | apt-key add -
RUN add-apt-repository "deb https://packages.grafana.com/oss/deb stable main"
RUN apt-get update && apt-get install -y grafana

# Exponemos puertos de Prometheus y Grafana
EXPOSE 9090 3000

# Iniciar servicios (Se necesitaria personalizar esto para producción)
CMD ["/bin/sh", "-c", "service grafana-server start && /bin/prometheus"]
