FROM grafana/grafana:8.4.5
USER root
COPY ./certs/grafana.crt /etc/grafana/grafana.crt
COPY ./certs/grafana.key /etc/grafana/grafana.key

RUN chown -R grafana:root /etc/grafana/grafana.crt && \
    chown -R grafana:root /etc/grafana/grafana.key && \
    chmod 400 /etc/grafana/grafana.key /etc/grafana/grafana.key
USER grafana