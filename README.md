# Sample application for tutorials

This repository contains the environment for completing the tutorials at [grafana.com/tutorials](https://grafana.com/tutorials).

## Prequisites

You will need to have the following installed locally to complete this workshop:

- [Docker](https://docs.docker.com/install/)
- [Docker Compose](https://docs.docker.com/compose/install/)

If you're running Docker for Desktop for macOS or Windows, Docker Compose is already included in your installation.

## Generate Certs

```bash
openssl genrsa -out grafana.key 2048
openssl req -new -key grafana.key -out grafana.csr
openssl x509 -req -days 365 -in grafana.csr -signkey grafana.key -out grafana.crt
```

## Running

To start the sample application and the supporting services:

```
docker-compose up -d
```

