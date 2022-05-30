# Postgres Docker Compose
Run postgres locally with docker-compose.

## Quick start
Change to the directory.
```bash
cd /path/to/postgres-docker-compose
```

Start the containers.
```bash
docker-compose up
```

_or_ 

Start the containers in "detached" mode.
```bash
docker-compose up -d
```

Stop the containers.
```bash
docker-compose down
```

## Services
🚧 Beware hardcoded credentials in `docker-compose.yml`.

The `docker-compose.yml` file consists of two services:
1. `postgres` - runs the postgres server
2. `pgadmin` - runs the pgadmin server


### Access postgres
The `postgres` service runs a postgres server. It is configured to auto-restart the container if it crashes.

- url: `http://localhost:5432`
- username: `postgres`
- password: `changeme`

### Access PgAdmin
The `pgadmin` service runs PgAdmin4. It is configured to auto-restart the container if it crashes.

- url: `http://localhost:5050`
- username: `pgadmin4@pgadmin.org`
- password: `admin`

### Add a new server in PgAdmin
- host name/address: `postgres`
- port: `5432`
- username: `postgres`
- password: `changeme`
