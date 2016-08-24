FROM phusion/baseimage
RUN export DEBIAN_FRONTEND=noninteractive && apt update && apt upgrade -y \
  && apt install -y apache2 php7.0* php-pear libapache2-mod-php7.0 \
  && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* \
  && mkdir /etc/service/apache2/
COPY ./apache2/run /etc/service/apache2/
