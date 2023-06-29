openssl req -x509 -sha256 -nodes -newkey rsa:2048 -days 365 -keyout localhost.key -out localhost.crt
openssl x509 -text -noout -in localhost.crt


1. Собрать образ
docker image build -t proxy_nginx_tls .

2. Создать контейнер
docker run --name proxy_nginx_tls -p 4433:443 -d proxy_nginx_tls
