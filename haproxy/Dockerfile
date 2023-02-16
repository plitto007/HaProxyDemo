FROM haproxy:1.6.15
# Create a system group and user to be used by HAProxy.
RUN set -eux; \
    groupadd --gid 99 --system haproxy; \
    useradd \
        --gid haproxy \
        --home-dir /var/lib/haproxy \
        --no-create-home \
        --system \
        --uid 99 \
        haproxy \
    ; \
    mkdir /var/lib/haproxy; \
    chown haproxy:haproxy /var/lib/haproxy
COPY haproxy.cfg /usr/local/etc/haproxy/haproxy.cfg