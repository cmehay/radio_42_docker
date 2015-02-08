FROM    debian:jessie

CMD     ["/usr/bin/ncmpcpp", "--host", "mpd"]

ADD     02apt-no-recom /etc/apt/apt.conf.d/

ENV     DEBIAN_FRONTEND noninteractive

RUN     apt-get -y update && apt-get -y ncmpcpp
