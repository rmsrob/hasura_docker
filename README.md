![name](https://miro.medium.com/max/1400/1*w91K4J_XoIM91S6aBE3mMQ.png)

# DOCKER-COMPOSE FOR HASURA

> local docker dev with Hasura

## Install

```bash
curl https://raw.githubusercontent.com/rmsrob/hasura_docker/docker-compose.yaml -o docker-compose.yml
```

## Prerequisite

> Create a file `.env` in the same level as your `docker-compose.yml`

```bash
PGSQL_HOST="app_pgsql"
PGSQL_PORT=54321
POSTGRES_DB="postgres"
POSTGRES_USER="postgres"
POSTGRES_PASSWORD="postgres"
HASURA_ADMIN="Yo!HasuraPassword"
```

## Usage

```bash
docker-compose up -d
```

> Head to [http://localhost:8080/console](http://localhost:8080/console) to open the Hasura console enter your HASURA_ADMIN pasword.

if you need to have a network inside your docker compose uncomment the block with it.
run once `docker network create app-netrunner` before docker-compose up.

## Maintainers

- [rmsrob][me]

[me]: https://github.com/rmsrob
