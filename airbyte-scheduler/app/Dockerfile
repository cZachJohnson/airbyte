ARG JDK_VERSION=14.0.2
FROM openjdk:${JDK_VERSION}-slim AS scheduler

ENV APPLICATION airbyte-scheduler

WORKDIR /app

ADD bin/${APPLICATION}-0.32.6-alpha.tar /app

# wait for upstream dependencies to become available before starting server
ENTRYPOINT ["/bin/bash", "-c", "${APPLICATION}-0.32.6-alpha/bin/${APPLICATION}"]
