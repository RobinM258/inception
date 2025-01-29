FROM alpine:3.20.4

RUN apk add nginx
RUN apk add vim

COPY conf/nginx.conf /etc/nginx/nginx.conf
RUN mkdir -p /etc/nginx/ssl
RUN apk add openssl
RUN openssl req -x509 -nodes -out /etc/nginx/ssl/inception.crt -keyout /etc/nginx/ssl/inception.key -subj "/C=FR/ST=IDF/L=PARIS/O=42/OU=42/CN=login.42.fr/UIND=login"
RUN mkdir -p /var/run/nginx
#RUN chmod 755 /var/www/html
#RUN chown -R www-data:www-data /var/www/html
CMD ["nginx", "-g", "daemon off;"]
