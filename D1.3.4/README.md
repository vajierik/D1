# Список команд

## Установка docker на хостах manager, worker1, worker2
curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

## Команды создания кластера на хосте manager
sudo docker swarm init --advertise-addr 10.128.0.34

### Проверка
sudo docker node ls

## Команды на хостах worker1, worker2
sudo docker swarm join --token SWMTKN-1-2nb0ezug4egnjas17xt8ety48edl5b6yhfzaac67gvpljf2asd-db3agl96it0wbzh789ed451sr 10.128.0.34:2377

This node joined a swarm as a worker.

## После выполнения команд на хостах worker проверка на manager
<<<<<<< HEAD
sudo docker node ls

## Перемещаем docker-compose.yml на хост manager в каталог переходим в него и запускаем команду
sudo docker stack deploy -c ./docker-compose.yml socks;
=======

sudo docker node ls

## Перемещаем docker-compose.yml на хост manager в каталог переходим в него и запускаем команду

sudo docker stack deploy -c ./docker-compose.yml socks;
>>>>>>> c96663931bf4255781783d5d3d9f84e0607b6793
