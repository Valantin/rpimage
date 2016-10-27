FROM armhf/alpine

MAINTAINER Roberto Valentini <valantin (at) gmail [dot] com>

RUN apk add --update rsyslog \
 && rm -rf /var/cache/apk/*

COPY ./etc/rsyslog.conf /etc/rsyslog.conf

EXPOSE 514 514/udp

VOLUME [ "/var/log", "/etc/rsyslog.d" ]

ENTRYPOINT [ "rsyslogd", "-n" ]
