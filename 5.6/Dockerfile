FROM alpine:3.6
MAINTAINER Billgo <cocobill@vip.qq.com>

RUN apk update && \
    apk add --no-cache ca-certificates && \
    apk add mysql mysql-client && \
    apk add tzdata && \
    ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone && \ 
    addgroup mysql mysql && \
    mkdir /scripts && \
    rm -rf /var/cache/apk/*

VOLUME ["/var/lib/mysql"]

COPY ./startup.sh /scripts/startup.sh
RUN chmod +x /scripts/startup.sh

EXPOSE 3306

ENTRYPOINT ["/scripts/startup.sh"]