FROM ubuntu

MAINTAINER Nick Payne <nick@kurai.co.uk>

RUN apt-get install -y wget build-essential

RUN wget http://download.redis.io/releases/redis-2.8.0.tar.gz
RUN tar xzf redis-2.8.0.tar.gz
RUN cd redis-2.8.0 && make

RUN mkdir /redis-data
VOLUME ["/redis-data"]

EXPOSE 6379

ENTRYPOINT ["/redis-2.8.0/src/redis-server"]
CMD ["--dir", "/redis-data"]
