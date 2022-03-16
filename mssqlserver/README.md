# MS SQL Server

Microsoft SQL server sample docker-compose. 

## Docker Compose

```yaml
version: "3.9"

services:
  mssqlserver:
    image: "mcr.microsoft.com/mssql/server:2019-latest"
    environment:
      SA_PASSWORD: "Password@123"
      ACCEPT_EULA: "Y"
    ports:
      - "1433:1433"

```

Once the container is running, the SQL server should be accessible through `localhost:1433`.

## Common Issues

### Password Policy

In order for the SQL server container to run you must ensure your SQL server password meet the SQL Server password policy requirements. The password must be at least 8 characters long and contain characters from three of the following four sets: Uppercase letters, Lowercase letters, Base 10 digits, and Symbols.