# Postgresql with pgAdmin

Sample docker-compose for Postgresql with pgAdmin.

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

  pgadmin:
    container_name: pgadmin
    image: dpage/pgadmin4
    depends_on:
      - postgres
    ports:
      - "53603:53603"
    environment:
      PGADMIN_DEFAULT_EMAIL: admin@example.com
      PGADMIN_DEFAULT_PASSWORD: root

```

Once the container is running, the postgresql and pgadmin should be accessible through `localhost:5432` and `localhost:53603` respectively.
