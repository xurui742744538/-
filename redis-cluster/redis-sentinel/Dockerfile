FROM redis:4.0.10-alpine

MAINTAINER xiaochunping <xcp.email@gmail.com>

ENV SENTINEL_QUORUM=2 
ENV SENTINEL_DOWN_AFTER=1000 
ENV SENTINEL_FAILOVER=1000 
ENV REDIS_PASSWORD=redis1234 

RUN mkdir -p /redis

WORKDIR /redis

COPY sentinel.conf .
COPY sentinel-entrypoint.sh /usr/local/bin/

RUN chown redis:redis /redis/* && \
    chmod +x /usr/local/bin/sentinel-entrypoint.sh

EXPOSE 26379

CMD ["sentinel-entrypoint.sh"]
