FROM lamp-prod
RUN export DEBIAN_FRONTEND=noninteractive && apt update && apt -y upgrade \
  && apt install -y build-essential python wget git \
  && wget https://deb.nodesource.com/setup_6.x && chmod +x setup_6.x && ./setup_6.x && apt install -y nodejs \
  && npm install forever -g \
  && cd / && git clone git://github.com/c9/core.git c9 && cd c9 && scripts/install-sdk.sh \
  && wget -O - https://raw.githubusercontent.com/c9/install/master/install.sh | bash \
  && mkdir /etc/service/cloud9 \
  && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /var/www/html/*
COPY ./cloud9/run /etc/service/cloud9/
