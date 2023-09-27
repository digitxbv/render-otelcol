FROM prom/prometheus

ADD prometheus.yml /etc/prometheus/
RUN mkdir -p /etc/config
ADD autometrics-rules.yml /etc/config/
