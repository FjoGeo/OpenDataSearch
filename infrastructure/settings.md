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

## PostgreSQL

```bash
docker exec -it postgres psql -U myuser -d mydb




```

## Other:

Since you defined your volumes as Named Volumes (like esdata: and pgdata:), Docker manages the storage for you in a specific area of your host system.

The exact location depends on which operating system you are using.

Linux /var/lib/docker/volumes/
