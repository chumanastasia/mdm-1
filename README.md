# mdm-1
Современные методы DevOps
### Задание 

 - Написать два докер-файла nginx и postgresql.

 - В конфиг **nginx** добавить возможность запрета POST запросов `limit_except POST { deny all; }`, а в конфиг базы постгреса добавить автоматическое создание пользователя `test` и пустой базы данных с тем же именем.

 - В качестве базового образа для **nginx** взять **alpine**, а в качестве базового образа для postgresql взять официальный с сайта [hub.docker.com]().

### Сборка и запуск контейнеров

- Сборка образа Nginx
```commandline
cd nginx/
docker build -t custom-nginx .
```

Сборка образа PostgreSQL
```commandline
cd postgresql/
docker build -t custom-postgres .
```

- Запуск контейнеров
```commandline
docker run -d -p 8080:80 custom-nginx
docker run -d -p 5432:5432 custom-postgres
```
