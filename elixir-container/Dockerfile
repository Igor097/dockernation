ARG ALPINE_VERSION=latest
FROM alpine:${ALPINE_VERSION}

LABEL maintainer="Madtuxx"

RUN apk upgrade && \
    apk --upgrade add --no-cache erlang && \
    apk --upgrade add --no-cache elixir && \
    rm -rf /var/cache/apk/* && \
    mkdir elixir-playground && \
    adduser -D madtuxx && \
    chown -R madtuxx /elixir-playground

USER madtuxx
WORKDIR elixir-playground/

CMD ["iex"]

