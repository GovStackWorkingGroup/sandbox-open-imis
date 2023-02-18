FROM ubuntu:18.04

#docker build -t db-image .

RUN apt-get update && apt-get install -y git
RUN git clone https://github.com/openimis/database_postgresql

# Script to detect whether the database has finished initializing
ADD ["https://github.com/openimis/database_postgresql/blob/8d60ef7cc17a4c88d49fce66ed31167346357572/true_isready.sh", "/usr/local/bin/"]
ADD ["https://github.com/openimis/database_postgresql/blob/2b106828fe6f76fadd8a61f6722abd71a9f94789/database%20scripts/00_dump.sql",  "/docker-entrypoint-initdb.d/"]
ADD ["https://github.com/openimis/database_postgresql/blob/2b106828fe6f76fadd8a61f6722abd71a9f94789/database%20scripts/02_aux_functions.sql",  "/docker-entrypoint-initdb.d/"]
ADD ["https://github.com/openimis/database_postgresql/blob/2b106828fe6f76fadd8a61f6722abd71a9f94789/database%20scripts/03_views.sql",  "/docker-entrypoint-initdb.d/"]
ADD ["https://github.com/openimis/database_postgresql/blob/2b106828fe6f76fadd8a61f6722abd71a9f94789/database%20scripts/04_functions.sql",  "/docker-entrypoint-initdb.d/"]
ADD ["https://github.com/openimis/database_postgresql/blob/2b106828fe6f76fadd8a61f6722abd71a9f94789/database%20scripts/05_stored_procs.sql",  "/docker-entrypoint-initdb.d/"]
ADD ["https://github.com/openimis/database_postgresql/blob/2b106828fe6f76fadd8a61f6722abd71a9f94789/database%20scripts/demo_db.sql",  "/docker-entrypoint-initdb.d/"]

ENV POSTGRES_PASSWORD=IMISuserP@s
ENV POSTGRES_DB=IMIS
ENV POSTGRES_USER=IMISuser
