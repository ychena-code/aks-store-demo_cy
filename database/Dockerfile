FROM postgres:13

ENV POSTGRES_USER=postgres
ENV POSTGRES_PASSWORD=yourpassword
ENV POSTGRES_DB=petstore

COPY init.sql /docker-entrypoint-initdb.d/

EXPOSE 5432
