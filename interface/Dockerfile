FROM    debian:jessie

CMD     ["/usr/bin/ncmpcpp", "--host", "mpd"]

ADD     apt-no-recom.conf /etc/apt/conf.d/

ENV     DEBIAN_FRONTEND noninteractive

RUN     apt-get -y update && apt-get -y ncmpcpp
