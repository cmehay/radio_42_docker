FROM    debian:jessie

CMD ["/usr/bin/supervisord"]

ADD     apt-no-recom.conf /etc/apt/conf.d/

ENV     DEBIAN_FRONTEND noninteractive

RUN	    apt-get -y update && apt-get -y install nginx at ca-certificates bzip2 \
            emacs24-nox faad flac git htop id3v2 id3 lame libav-tools \
            mpc mpd ncmpcpp php5-cli php5-cli php5-fpm pulseaudio sox \
            supervisor swh-plugins vlc-nox vorbis-tools wget

ADD     init /init
ADD     mpd.conf /etc/mpd.conf
ADD     supervisord.conf /etc/supervisor/conf.d/supervisord.conf
ADD     system.pa /etc/pulse/system.pa

EXPOSE  80 8080 6600
