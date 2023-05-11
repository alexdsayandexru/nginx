docker image build -t go_hello_world .

docker run --rm --name go_hello_world_1 -p 8081:8888 go_hello_world
docker run --rm --name go_hello_world_2 -p 8082:8888 go_hello_world
docker run --rm --name go_hello_world_3 -p 8083:8888 go_hello_world
