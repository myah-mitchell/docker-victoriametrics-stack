# Docker VictoriaMetrics Stack


## Create needed folders

```bash
mkdir -p /opt/docker/volumes/victoria/victorialogs-data
mkdir -p /opt/docker/volumes/victoria/victoriametrics-data
mkdir -p /opt/docker/volumes/victoria/grafana-data
chmod -R 770 /opt/docker/volumes/victoria/*
sudo chown $USER:101000 /opt/docker/volumes/victoria
sudo chown -R 101000:101000 /opt/docker/volumes/victoria/*
```

