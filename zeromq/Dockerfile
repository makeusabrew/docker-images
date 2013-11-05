FROM ubuntu

MAINTAINER Nick Payne <nick@kurai.co.uk>

RUN apt-get install -y wget build-essential

RUN wget http://download.zeromq.org/zeromq-3.2.4.tar.gz
RUN tar xzf zeromq-3.2.4.tar.gz
WORKDIR /zeromq-3.2.4
RUN ./configure && make && make install
RUN ldconfig
