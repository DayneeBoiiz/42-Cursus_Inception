FROM debian:buster

RUN apt-get update -y;\
	apt-get install redis -y;\
	sed -i 's/bind 127.0.0.1/bind 0.0.0.0/g' /etc/redis/redis.conf

ENTRYPOINT ["redis-server", "--protected-mode no"]