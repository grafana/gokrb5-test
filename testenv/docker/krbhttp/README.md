# HTTPD Integration Test Instance for TEST.GOKRB5

DO NOT USE THIS CONTAINER FOR ANY PRODUCTION USE!!!

To run:
```bash
docker run -v /etc/localtime:/etc/localtime:ro -p 80:80 -p 443:443 --rm --name gokrb5-http grafana/gokrb5-test:http &
```

To build:
```bash
docker build -t ghcr.io/grafana/gokrb5-test:http --force-rm=true --rm=true .
docker push ghcr.io/grafana/gokrb5-test:http
```


