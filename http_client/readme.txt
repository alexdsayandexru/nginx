1. Собрать образ
docker image build -t client_nginx .

2. Создать контейнер
docker run --name client_nginx -p 9191:80 -d client_nginx
