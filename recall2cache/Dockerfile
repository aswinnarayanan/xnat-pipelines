FROM ubuntu:24.04

ARG RECALL2CACHE_VERSION=2025.08.14

RUN apt-get update && \
    apt-get install -y --no-install-recommends curl && \
    curl -L -o recall2cache-linux-amd64.tar.gz https://github.com/aswinnarayanan/recall2cache/releases/download/${RECALL2CACHE_VERSION}/recall2cache-linux-amd64.tar.gz && \
    tar -xzf recall2cache-linux-amd64.tar.gz && \
    mv recall2cache /usr/local/bin/ && \
    chmod +x /usr/local/bin/recall2cache && \
    apt-get purge -y --auto-remove curl && \
    rm recall2cache-linux-amd64.tar.gz && \
    rm -rf /var/lib/apt/lists/*
