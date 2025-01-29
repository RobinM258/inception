FROM alpine3.20.4

RUN apk update
RUN apk upgrade
RUN apk add wget

RUN apt-get install -y php7.3\
	php-fpm\
	php-mysql\
	mariadb-client
RUN wget https://fr.wordpress.org/wordpress-6.0-fr_FR.tar.gz -P /var/www
					