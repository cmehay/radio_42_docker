FROM    debian:jessie

CMD     ["/usr/bin/supervisord", "-n"]

ADD     02apt-no-recom /etc/apt/apt.conf.d/

ENV     DEBIAN_FRONTEND noninteractive

RUN	    apt-get -y update && apt-get -y install nginx at ca-certificates bzip2 \
            emacs24-nox faad flac git htop id3v2 id3 lame libav-tools \
            mpc mpd ncmpcpp php5-cli php5-cli php5-fpm pulseaudio sox \
            supervisor swh-plugins vlc-nox vorbis-tools wget

ADD     init /init
ADD     mpd.conf /etc/mpd.conf
ADD     supervisord.conf /etc/supervisor/conf.d/supervisord.conf
ADD     system.pa /etc/pulse/system.pa
ADD     daemon.conf /etc/pulse/daemon.conf
ADD     nginx.conf /etc/nginx/sites-available/radio42
ADD     silent.ogg /silent.ogg
RUN     ln -s /etc/nginx/sites-available/radio42 /etc/nginx/sites-enabled/radio42
RUN     rm /etc/nginx/sites-enabled/default
ADD     opt /opt

USER    www-data
RUN     git clone https://github.com/cmehay/radio_42.git /var/www/radio42/

USER    root

EXPOSE  80 8080 6600
