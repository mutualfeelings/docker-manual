# Образы Docker 

Построение образа из Dockerfile

`docker build -t image_name path_to_dockerfile`

Список всех локальных образов

`docker images`

Скачивание образа из DockerHub

`docker pull image_name:tag`

Удаление локального образа

`docker rmi image_name:tag`

Добавление тега для образа

`docker tag source_image:tag new_image:tag`

Загрузить образ на DockerHub

`docker push image_name:tag`

Посмотреть детали образа

`docker image inspect image_name:tag`

Сохранить образ в tar-архив

`docker save -o image_name.tar image_name:tag`

Загрузить образ из tar-архива

`docker load -i image_name.tar`

Удалить неиспользуемые образы

`docker image prune `

# Docker Containers

Запустить контейнер на основе образа

`docker run container_name image_name`

Запустить именованный контейнер из образа

`docker run --name container_name image_name:tag`

Вывести список всех контейнеров (включая остановленные)
`docker ps -a`

Остановить запущенный контейнер

`docker stop container_name_or_id`

Запустить остановленный контейнер

`docker start container_name_or_id`

Запустить контейнер в интерактивном режиме

`docker run -it container_name_or_id`

Запустить контейнер в интерактивном режиме с shell:

`docker run -it container_name_or_id /bin/bash`

Удалить остановленный контейнер

`docker rm container_name_or_id`

Посмотреть детали контейнера

`docker inspect container_name_or_id`

Просмотреть логи контейнера

`docker logs container_name_or_id`

Приостановить работу запущенного контейнера

`docker pause container_name_or_id`

Возобновить работу приостановленного контейнера

`docker unpause container_name_or_id`

# Тома Docker и Сеть

Создать именованный volume

`docker volume create volume_name`

Вывести список всех volumes

`docker volume ls`

Посмотреть детали volume

`docker volume inspect volume_name`

Удалить volume

`docker volume rm volume_name`

Запустить контейнер с volume (mount)

`docker run --name container_name -v volume_name:/path/in/container image_name:tag`

Копировать файлы между контейнером и volume

`docker cp local_file_or_directory container_name:/path/in/container`

Запустить контейнер с маршрутизацией портов

`docker run --name container_name -p host_port:container_port image_name`

Вывести список всех сетей

`docker volume ls`

Посмотреть детали сети

`docker network inspect network_name`

Создать пользовательскую мостовую сеть

`docker network create network_name`

Подключить контейнер к сети

`docker network connect network_name container_name`

Отключить контейнер от сети

`docker network disconnect network_name container_name`

# Docker Compose

Создать и запустить контейнеры, определенные в файле docker-compose.yml

`docker compose up`

Остановить и удалить контейнеры, определенные в файле docker-compose.yml

`docker compose down`

Собрать или пересобрать сервисы

`docker compose build`

Вывести список контейнеров для определенного проекта Docker Compose

`docker compose ps`

Просмотреть логи сервисов

`docker compose logs`

Масштабировать сервисы до определенного количества контейнеров:

`docker compose up -d --scale service_name=number_of_containers`

Выполнить одноразовую команду в сервисе

`docker compose run service_name command`

Просмотреть детали сервиса

`docker compose ps service_name`









