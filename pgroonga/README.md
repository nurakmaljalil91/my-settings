## Dockerfile for PGroonga

Dockerfile for great PostgreSQL full text search extension [PGroonga](https://github.com/pgroonga/pgroonga)

Those images based on [postgres](https://hub.docker.com/_/postgres) and could use as same as `postgres` images

## Quick start

```shell
  docker run -d groonga/pgroonga
```

## How to use

Here is a simple example for use by [docker-compose](https://github.com/docker/compose).

Create `docker-compose.yml` with lines below.

```docker-compose
version: '2'
services:
  PGroonga:
    image: groonga/pgroonga:latest
    ports:
      - 5432:5432
    environment:
      POSTGRES_DB: PGroonga
      POSTGRES_PASSWORD: PGroonga
      POSTGRES_USER: PGroonga
```

now You can use `docker-compose up -d` command to start service.
by use any database manage tool to connect to database `PGroonga`,exceute command below to active PGroonga extension

```SQL
create extension pgroonga;
```

please take a look at [PGroonga website](https://pgroonga.github.io/) for details

