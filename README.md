# Docker образ для MapStore 2

## Описание

Этот репозиторий содержит Dockerfile и необходимые файлы для создания Docker образа MapStore 2. MapStore 2 - это современная геопространственная платформа, предназначенная для создания и публикации интерактивных карт и геоинформационных приложений.

## Использование

### MapStore2

- Склонируйте репозиторий:
    ```commandline
    git clone https://github.com/VladislavGolubtsov/mapstore2_ru_local.git
    ```
- Перейдите в папку репозитория:
    ```commandline
    cd mapstore2_ru_local
    ```
- Для сборки образа и запуска контейнера выполните:
    ```commandline
    docker-compose up -d
    ```
После того как контейнер запустился, перейдите на сайт http://localhost:8080/mapstore/ для проверки работоспособности (для входа в личный кабинет используйте логин: `admin`, пароль `admin`).

### GeoServer

- Загрузите из Docker Hub образ geoserver:
    ```commandline
    docker pull docker.osgeo.org/geoserver:2.24.1
    ```
- Запустите Docker образ GeoServer:
    ```commandline
    docker run -d -p 8081:8080 docker.osgeo.org/geoserver:2.24.1
    ```
Когда контейнер будет запущен, перейдите на сайт http://localhost:8081/geoserver/web для проверки работоспособности GeoServer (для входа в личный кабинет используйте логин: `admin`, пароль `geoserver`).

### О сборке

Скоро будет обновление с уменьшением веса контейнеров и собственной сборкой GeoServer