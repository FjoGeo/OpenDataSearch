# Settings for ES

## Increase Virtual Memory Limit

```bash

sudo sysctl -w vm.max_map_count=262144
```

## Start Docker

```bash

# go to the 'infrastructure' directory

docker compose up -d

# shutdown docker
docker compose down

# check logstash
docker logs -f logstash
```
