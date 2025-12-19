FROM ubuntu:noble
ARG GO_VERSION=1.25.5
#ARG GO_ARCH=amd64
ARG GO_ARCH=arm64
USER root
RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y curl && \
    curl -fsSL "https://go.dev/dl/go${GO_VERSION}.linux-${GO_ARCH}.tar.gz" -o go.tar.gz && \
    tar -C /usr/local -xzf go.tar.gz && \
    rm go.tar.gz

ENV PATH="/usr/local/go/bin:${PATH}"
CMD ["sleep", "infinity"]