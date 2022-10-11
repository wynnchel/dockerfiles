FROM nginx:stable
RUN apt-get update && apt-get install -y openssl php php-fpm
RUN mkdir -p /etc/nginx/ssl && mkdir -p /srv/data && \
  mkdir -p /run/php/php7.4-fpm.sock

COPY default.conf /etc/nginx/conf.d/
COPY start.sh /
ENTRYPOINT [ "/start.sh" ]
