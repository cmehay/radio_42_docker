FROM    busybox

RUN     mkdir /music /playlist /syncthing

RUN     chmod 777 /music /playlist
RUN     chown 800:800 /syncthing

VOLUME  /music
VOLUME  /playlist
VOLUME  /syncthing

CMD     ["true"]
