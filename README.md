# Notas_postgresql

Administración SQL (PostgreSQL y SQL Server)
#1-	Tamaño de las bases de datos PSQL:
SELECT
pg_database.datname,
pg_size_pretty(pg_database_size(pg_database.datname)) AS size
FROM pg_database;

#2-	Cambiar la contraseña de un usuario PSQL:
ALTER USER usuario WITH PASSWORD 'contraseña';

#3- Crear un usuario en PSQL

CREATE USER myuser WITH PASSWORD 'secret_passwd';

#4- Crear un Rol en PSQL

CREATE ROLE myuser WITH LOGIN PASSWORD 'secret_passwd';

#5-  Crear un Rol de lectura

CREATE ROLE readonly;

-Conectar Rol con BD:

GRANT CONNECT ON DATABASE mydatabase TO readonly;
-Dar permisos al rol con la BD
GRANT USAGE ON SCHEMA myschema TO readonly;

