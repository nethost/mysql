FROM nethost/alpine:latest
MAINTAINER Billgo <cocobill@vip.qq.com>

RUN addgroup mysql mysql && \
    apk update && \
    apk add --no-cache mysql mysql-client && \
    rm -rf /var/cache/apk/*

VOLUME ["/var/lib/mysql"]

COPY ./entrypoint.sh /

EXPOSE 3306

ENTRYPOINT ["/entrypoint.sh"]