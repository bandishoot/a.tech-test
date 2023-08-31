FROM debian:latest

RUN apt update -y && apt install -y ca-certificates curl procps iproute2 redis 

RUN apt-get autoremove --purge -y curl && \
    apt-get update && apt-get upgrade -y && \
    apt-get clean && rm -rf /var/lib/apt/lists /var/cache/apt/archives

EXPOSE 6379
CMD ["redis-server","/usr/local/etc/redis/redis.conf","daemonize no"]
