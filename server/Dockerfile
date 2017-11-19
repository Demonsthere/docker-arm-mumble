FROM armv7/armhf-ubuntu:latest
MAINTAINER daemonsthere@gmail.com

RUN useradd -u 1000 -d /opt/mumble -m -s /bin/bash mumble &&\
  apt-get update &&\
  apt-get install -y mumble-server &&\
  apt-get -y autoremove &&\
  apt-get -y autoclean &&\
  apt-get -y clean

ADD files/mumble-server.ini /opt/mumble/mumble-server.ini

EXPOSE 64738/udp
USER mumble

ENTRYPOINT ["murmurd"]
CMD ["-fg", "-ini", "/opt/mumble/mumble-server.ini"]
