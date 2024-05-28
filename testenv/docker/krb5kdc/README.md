# KDC Integration Test Instance for TEST.GOKRB5

DO NOT USE THIS CONTAINER FOR ANY PRODUCTION USE!!!

To run:
```bash
docker run -v /etc/localtime:/etc/localtime:ro -p 88:88 -p 88:88/udp -p 464:464 -p 464:464/udp --rm --name gokrb5-kdc-centos-default grafana/gokrb5-test:kdc-centos-default &
```

To build:
```bash
docker build -t ghcr.io/grafana/gokrb5-test:kdc-centos-default --force-rm=true --rm=true .
docker push ghcr.io/grafana/gokrb5-test:kdc-centos-default
```


