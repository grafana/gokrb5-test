# KDC Integration Test Instance for RESDOM.GOKRB5

DO NOT USE THIS CONTAINER FOR ANY PRODUCTION USE!!!

To run:
```bash
docker run -v /etc/localtime:/etc/localtime:ro -p 188:88 -p 188:88/udp --rm --name gokrb5-res grafana/gokrb5-test:kdc-resdom &
```

To build:
```bash
docker build -t ghcr.io/grafana/gokrb5-test:kdc-resdom --force-rm=true --rm=true .
docker push ghcr.io/grafana/gokrb5-test:kdc-resdom
```


