ARG BUILD_FROM=hassioaddons/base:6.0.1
# hadolint ignore=DL3006
FROM ${BUILD_FROM}


RUN apk --no-cache add \
	openvpn


# Build arguments
ARG BUILD_ARCH
ARG BUILD_DATE
ARG BUILD_REF
ARG BUILD_VERSION

WORKDIR /etc/openvpn
ENTRYPOINT ["openvpn", "--config", "/config/openvpn-client/client.ovpn"]
