# Docker Databases Sql NoSql Configuration

### <img src="https://user-images.githubusercontent.com/55373948/236650481-980cb882-e257-4590-ad0a-3ee13c907dd9.png" alt="PostgresSql" width="20" height="20"> Postgres Latest  
```sh
docker run --name postgres-latest -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=postgres -dp 5432:5432 postgres 
```
### MariaDb
```sh
docker container run -dp 3306:3306 \
--name world-db \
--env MARIADB_USER=mariadb_user \
--env MARIADB_PASSWORD=mariadb_user \
--env MARIADB_ROOT_PASSWORD=root-mariadb-user \
--env MARIADB_DATABASE=world-db \
mariadb:jammy
```

### MariaDb Windows PowerShell
```sh
docker container run -dp 3306:3306 `
--name world-db `
--env MARIADB_USER=mariadb_user `
--env MARIADB_PASSWORD=mariadb_user `
--env MARIADB_ROOT_PASSWORD=root-mariadb-user `
--env MARIADB_DATABASE=world-db `
mariadb:jammy
```

### Azure SQL Edge
```
docker pull mcr.microsoft.com/azure-sql-edge
```


#### Configurar Imagen
```sh
docker run --cap-add SYS_PTRACE -e 'ACCEPT_EULA=Y' -e 'MSSQL_SA_PASSWORD=MY_STRONG_Password10!' -p 1433:1433 --name azuresqledge -d mcr.microsoft.com/azure-sql-edge
```
#### Configurar Imagen Premium
```sh
docker run --cap-add SYS_PTRACE -e 'ACCEPT_EULA=1' -e 'MSSQL_SA_PASSWORD=MY_STRONG_Password10!' -e 'MSSQL_PID=Premium' -p 1433:1433 --name azuresqledge -d mcr.microsoft.com/azure-sql-edge
```
