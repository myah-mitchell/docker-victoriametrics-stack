# Docker VictoriaMetrics Stack

This stack was created from the example configs provided by VictroaMetrics at:
* https://github.com/VictoriaMetrics/VictoriaLogs/tree/master/deployment/docker
* https://github.com/VictoriaMetrics/VictoriaMetrics/tree/master/deployment/docker
* https://github.com/VictoriaMetrics/VictoriaTraces/tree/master/deployment/docker

Install node-exporter on each host by following:
* https://docs.techdox.nz/node-exporter/

## Create needed folders for server

```bash
mkdir -p /opt/docker/volumes/victoriametrics/victorialogs-data
mkdir -p /opt/docker/volumes/victoriametrics/victoriametrics-data
mkdir -p /opt/docker/volumes/victoriametrics/victoriatraces-data
mkdir -p /opt/docker/volumes/victoriametrics/vmagent-data
mkdir -p /opt/docker/volumes/victoriametrics/vlagent-data
mkdir -p /opt/docker/volumes/victoriametrics/grafana-data
chmod -R 770 /opt/docker/volumes/victoriametrics/*
sudo chown $USER:101000 /opt/docker/volumes/victoriametrics
sudo chown 101000:101000 /opt/docker/volumes/victoriametrics/*
```

## Create needed folders for agent

```bash
mkdir -p /opt/docker/volumes/victoriametrics-agent/vmagent-data
mkdir -p /opt/docker/volumes/victoriametrics-agent/vlagent-data
chmod -R 770 /opt/docker/volumes/victoriametrics-agent/*
sudo chown $USER:101000 /opt/docker/volumes/victoriametrics-agent
sudo chown 101000:101000 /opt/docker/volumes/victoriametrics-agent/*
```