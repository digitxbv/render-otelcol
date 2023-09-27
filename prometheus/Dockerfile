FROM prom/prometheus

USER root
RUN mkdir -p /etc/config
USER nobody

ADD prometheus.yml /etc/prometheus/
ADD autometrics-rules.yml /etc/config/
