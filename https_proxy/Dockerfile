FROM nginx

RUN \
  apt-get update && \
  apt-get install -y \
    vim

COPY default_1.conf /etc/nginx/conf.d/default.conf
COPY localhost.crt /etc/nginx/localhost.crt
COPY localhost.key /etc/nginx/localhost.key
