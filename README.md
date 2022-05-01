# Elastic Stack with Docker

## Installation

```shell 
docker-compose up -d
```

* Wait five minutes to setup

```shell 
docker cp es01:/usr/share/elasticsearch/config/certs/http_ca.crt .
```

```shell 
curl --cacert http_ca.crt -u elastic https://localhost:9200
```

```shell 
docker exec -it es01 bin/elasticsearch-create-enrollment-token --scope kibana
```

```shell 
docker logs kib01
```

## Stop

```shell
docker-compose stop
```

## Start

```shell
docker-compose start
```