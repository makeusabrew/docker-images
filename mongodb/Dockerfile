FROM ubuntu

MAINTAINER Nick Payne <nick@kurai.co.uk>

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10
RUN echo 'deb http://downloads-distro.mongodb.org/repo/ubuntu-upstart dist 10gen' | tee /etc/apt/sources.list.d/10gen.list

RUN dpkg-divert --local --rename --add /sbin/initctl
RUN ln -s /bin/true /sbin/initctl

RUN apt-get update
RUN apt-get -y install mongodb-10gen

RUN mkdir -p /data/db
VOLUME ["/data/db"]

EXPOSE 27017

ENTRYPOINT ["usr/bin/mongod"]
