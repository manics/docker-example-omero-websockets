FROM docker.io/library/alpine:3.6

RUN apk add --no-cache \
    openssl

ADD certs.sh /usr/local/bin/certs.sh

# Certificates are written to the current working directory
WORKDIR /icessl
ENTRYPOINT ["/usr/local/bin/certs.sh"]
