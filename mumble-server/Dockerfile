FROM alpine

RUN mkdir /opt && \
    wget -q -O- https://github.com/mumble-voip/mumble/releases/download/1.2.19/murmur-static_x86-1.2.19.tar.bz2 | tar -xj -C /opt

WORKDIR /opt/murmur-static_x86-1.2.19

EXPOSE 64738/tcp 64738/udp

CMD ["./murmur.x86", "-fg", "-ini", "/config/murmur.ini"]

VOLUME /config
