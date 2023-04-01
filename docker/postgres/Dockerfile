FROM postgres
# Install PostGIS packages
RUN apt-get update
RUN apt-get install --no-install-recommends --yes \
    postgresql-10-postgis-2.4 postgresql-10-postgis-2.4-scripts postgresql-contrib

#COPY ./sql/create_tables.sql /docker-entrypoint-initdb.d/