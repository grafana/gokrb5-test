# KDC Integration Test Instance for SUB.TEST.GOKRB5

DO NOT USE THIS CONTAINER FOR ANY PRODUCTION USE!!!

To run:
```bash
docker run -v /etc/localtime:/etc/localtime:ro -p 288:88 -p 188:88/udp --rm --name gokrb5-kdc-sub grafana/gokrb5-test:kdc-sub &
```

To build:
```bash
docker build -t ghcr.io/grafana/gokrb5-test:kdc-sub --force-rm=true --rm=true .
docker push ghcr.io/grafana/gokrb5-test:kdc-sub
```


