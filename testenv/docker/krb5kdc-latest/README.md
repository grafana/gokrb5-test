# KDC Integration Test Instance for TEST.GOKRB5

DO NOT USE THIS CONTAINER FOR ANY PRODUCTION USE!!!

To run:
```bash
docker run -v /etc/localtime:/etc/localtime:ro -p 98:88 -p 98:88/udp --rm --name gokrb5-kdc-latest grafana/gokrb5-test:kdc-latest &
```

To build:
```bash
docker build -t ghcr.io/grafana/gokrb5-test:kdc-latest --force-rm=true --rm=true .
docker push ghcr.io/grafana/gokrb5-test:kdc-latest
```
