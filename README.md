# Docker Databases Sql NoSql Configuration

### Postgres Latest
```sh
docker run --name -d postgres-latest -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=postgres -p 5432:5432 postgres 
```

### Azure SQL Edge
```
docker pull mcr.microsoft.com/azure-sql-edge
```

#### Configurar Imagen
```sh
docker run --cap-add SYS_PTRACE -e 'ACCEPT_EULA=Y' -e 'MSSQL_SA_PASSWORD=MY_STRONG_Password10!' -p 1433:1433 --name azuresqledge -d mcr.microsoft.com/azure-sql-edge
```
Configurar Imagen Premium
```sh
docker run --cap-add SYS_PTRACE -e 'ACCEPT_EULA=1' -e 'MSSQL_SA_PASSWORD=MY_STRONG_Password10!' -e 'MSSQL_PID=Premium' -p 1433:1433 --name azuresqledge -d mcr.microsoft.com/azure-sql-edge
```
