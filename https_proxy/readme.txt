openssl req -x509 -sha256 -nodes -newkey rsa:2048 -days 365 -keyout localhost.key -out localhost.crt
openssl x509 -text -noout -in localhost.crt
sudo security add-trusted-cert -d -r trustRoot -k /Library/Keychains/System.keychain /Users/aleksandrsudakov/GolandProjects/nginx/https_proxy/localhost.crt

1. Собрать образ
docker image build -t proxy_nginx_tls .

2. Создать контейнер
docker run --name proxy_nginx_tls -p 9393:443 -d proxy_nginx_tls
