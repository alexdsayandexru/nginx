1. Собрать образ
docker image build -t load_balancer_nginx .

2. Создать контейнер
docker run --name load_balancer_nginx -p 9999:80 -d load_balancer_nginx

3. Выполнить запросы к балансировщику
while sleep 0.5; do curl http://localhost:9999; done