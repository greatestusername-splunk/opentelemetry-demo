FROM gvenzl/oracle-xe:21-slim-faststart

ENV ORACLE_PASSWORD=password

ENV APP_USER=otel
ENV APP_USER_PASSWORD=password

RUN mkdir -p /container-entrypoint-initdb.d

COPY initOracleDB.sql /container-entrypoint-initdb.d/startup.sql

HEALTHCHECK CMD "$ORACLE_BASE/healthcheck.sh"