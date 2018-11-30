FROM alpine:3.8
LABEL maintainer="Billgo <cocobill@vip.qq.com>"

RUN apk update && \
    apk add --no-cache mysql mysql-client && \
    addgroup mysql mysql && \
    rm -rf /var/cache/apk/* && \
    chown -R mysql:mysql /var/lib/mysql

VOLUME /var/lib/mysql

COPY ./entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

EXPOSE 3306

ENTRYPOINT ["/entrypoint.sh"]