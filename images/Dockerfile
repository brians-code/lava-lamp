FROM php:7-apache
RUN export DEBIAN_FRONTEND=noninteractive \
  && apt update \
  && apt upgrade -y \
  && apt install -y git mysql-server \
  && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /var/www/html/*
