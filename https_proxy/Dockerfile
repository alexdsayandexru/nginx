FROM nginx:latest

RUN \
  apt-get update && \
  apt-get install -y \
    vim

COPY default.conf /etc/nginx/conf.d/default.conf
COPY localhost.crt /etc/nginx/localhost.crt
COPY localhost.key /etc/nginx/localhost.key
