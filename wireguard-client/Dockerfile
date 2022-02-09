ARG BUILD_FROM=ghcr.io/hassio-addons/base/amd64:11.0.1
# hadolint ignore=DL3006
FROM ${BUILD_FROM}


RUN apk --no-cache add \
    wireguard-tools\
    openresolv


# Build arguments
ARG BUILD_ARCH
ARG BUILD_DATE
ARG BUILD_DESCRIPTION
ARG BUILD_NAME
ARG BUILD_REF
ARG BUILD_REPOSITORY
ARG BUILD_VERSION

WORKDIR /etc/wireguard
ENTRYPOINT ["wg-quick", "up",  "/config/wireguard-client/peer.conf"]