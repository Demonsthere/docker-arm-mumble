FROM armv7/armhf-ubuntu:latest
MAINTAINER daemonsthere@gmail.com

RUN apt-get update &&\
  apt-get install -y mumble-server &&\
  apt-get -y autoremove &&\
  apt-get -y autoclean &&\
  apt-get -y clean

ADD files/mumble-server.ini /opt/mumble/mumble-server.ini

EXPOSE 64738/udp

ENTRYPOINT ["murmurd"]
CMD ["-fg", "-ini", "/opt/mumble/mumble-server.ini"]
