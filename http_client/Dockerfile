FROM nginx

RUN \
  apt-get update && \
  apt-get install -y \
    vim

COPY default.conf /etc/nginx/conf.d/default.conf
COPY index.html /usr/share/nginx/html/index.html


