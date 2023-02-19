FROM postgres:13-alpine

# Script to detect whether the database has finished initializing
COPY ["true_isready.sh", "/usr/local/bin/"]
COPY ["migrations/00_dump.sql", "migrations/0[2345]_*.sql", "migrations/demo_db.sql", "/docker-entrypoint-initdb.d/"]

#
ENV POSTGRES_PASSWORD=IMISuserP@s
ENV POSTGRES_DB=IMIS
ENV POSTGRES_USER=IMISuser
