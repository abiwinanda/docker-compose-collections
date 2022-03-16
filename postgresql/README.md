# Postgresql

Sample docker-compose for Postgresql.

## Docker Compose

```yaml
version: '3'

services:
  postgres:
    container_name: postgres
    image: postgres:12-alpine
    environment:
      POSTGRES_USER: postgres
      POSTGRES_PASSWORD: postgres
      PGDATA: /var/lib/postgresql/data/pgdata
    restart: always
    ports:
      - "5432:5432"

```

Once the container is running, the postgresql should be accessible through `localhost:5432`.
