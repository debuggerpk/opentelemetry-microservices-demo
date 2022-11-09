# FROM otel/opentelemetry-collector-contrib:0.45.0
FROM ubuntu:jammy
# COPY conf.yml .
COPY ext-conf.yml .
COPY otel-build/* ./otel-build/

EXPOSE 1888
EXPOSE 8888
EXPOSE 8889
EXPOSE 13133
EXPOSE 4317
EXPOSE 55670

# CMD [ "--config=conf.yml" ]
ENTRYPOINT ./otel-build/otel_with_custom_auth --config=ext-conf.yml