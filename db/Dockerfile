FROM postgres:latest

COPY ./test_db.sql /docker-entrypoint-initdb.d/

ENV POSTGRES_PASSWORD=secretpassword

