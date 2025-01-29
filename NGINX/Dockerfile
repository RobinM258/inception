FROM debian:buster

RUN apt update
RUN apt install nginx -y 
RUN apt install vim -y
RUN mkdir -p /etc/nginx/ssl
RUN apt install OpenSSL -y
RUN -subj openssl req -x509 -nodes -out /etc/nginx/ssl/inception.crt -keyout /etc/nginx/ssl/inception.key -subj "/C=FR/ST=IDF/L=Mulhouse/O=42/OU=42/CN=login.42.fr/UID=romartin" 