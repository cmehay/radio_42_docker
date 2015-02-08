FROM    busybox

RUN     mkdir /music /playlist /syncthing

VOLUME  /music
VOLUME  /playlist
VOLUME  /syncthing

RUN     chmod 777 /music /playlist
RUN     chown 800:800 /syncthing

CMD     ["/usr/bin/true"]
