FROM alpine:3.20.4

RUN apk update
RUN apk upgrade
RUN apk add mariadb mariadb-client
COPY conf/50-server.cnf	/etc/mysql/mariadb.conf.d/50-server.cnf

ADD /script.sh ./script.sh

ENTRYPOINT [ "/script.sh" ]
