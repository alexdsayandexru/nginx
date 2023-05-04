1. Собрать образ
docker image build -t proxy_nginx .

2. Создать контейнер
docker run --name proxy_nginx -p 9292:80 -d proxy_nginx
