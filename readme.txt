sudo security add-trusted-cert -d -r trustRoot -k /Library/Keychains/System.keychain /Users/aleksandrsudakov/GolandProjects/nginx/https_proxy/localhost.crt

1. Собрать образ
docker image build -t proxy_nginx .

2. Создать контейнер
docker run --name proxy_nginx -p 9090:80 -d proxy_nginx

3. Зайти в контейнер
docker exec -it proxy_nginx bash
4. cat /etc/nginx/conf.d/default.conf
5. cat /var/log/nginx/proxy_nginx-error.log

ls -l /etc/nginx/

apt-get update
apt-get install vim

/etc/nginx/conf.d/default.conf
service nginx reload


https://ssl-config.mozilla.org/

--Какие порты заняты
sudo lsof -iTCP -sTCP:LISTEN -n -P
==============