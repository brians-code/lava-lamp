FROM phusion/baseimage:0.9.19
CMD ["/sbin/my_init"]
RUN export DEBIAN_FRONTEND=noninteractive \
  && apt update \
  && apt install -y apt-utils \
  && apt upgrade -y \
  && apt install -y git mysql-server apache2 php7.0* libapache2-mod-php7.0 \
  && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /var/www/html/*
COPY rc.local /etc/rc.local
RUN chmod +x /etc/rc.local
