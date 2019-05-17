FROM mariadb/server:10.3
# Add a database
ENV MYSQL_DATABASE wiki
# executed during container startup
COPY ./sql-scripts/ /docker-entrypoint-initdb.d/
