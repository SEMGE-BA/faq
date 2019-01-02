## [Comandos Docker](./comando_docker.md)

## Montando o ambiente com Docker

Entre na pasta do projeto e crie os seguintes arquivos: `Dockerfile` e `docker-compose.yaml`

No `Dockerfile` digite:

```
FROM semgeba/oracle-php7
ADD . $DIR
RUN composer update
CMD php artisan serve --host 0.0.0.0 --port $PORT --env=$APP_ENV
```

No `docker-compose.yaml` digite:

```yaml
version: '2'
services:
    web:
        build: .
        volumes:
            - .:/var/www/html/
        environment:
            - PORT=8000
            - APP_ENV=local
        ports:
            - "8000:8000"
        depends_on:
            - db
    db:
        image: mysql
        environment:
            - MYSQL_ROOT_PASSWORD=true
            - MYSQL_DATABASE=[db_name]
        ports:
            - "3306:3306"
```


#### Executando o projeto

`docker compose up`


#### Executando comandos dentro do container

`docker-compose run --rm web [command]`
