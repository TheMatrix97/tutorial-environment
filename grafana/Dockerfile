FROM grafana/grafana:8.4.5
USER root

RUN openssl req -new -newkey rsa:4096 -days 365 -nodes -x509 \
    -subj "/C=US/ST=Denial/L=Springfield/O=Dis/CN=localhost" \
    -keyout /etc/grafana/grafana.key  -out /etc/grafana/grafana.crt

RUN chown -R grafana:root /etc/grafana/grafana.crt && \
    chown -R grafana:root /etc/grafana/grafana.key && \
    chmod 400 /etc/grafana/grafana.key /etc/grafana/grafana.key
USER grafana