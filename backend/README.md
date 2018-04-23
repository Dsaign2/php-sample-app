## Build

Para fazer a build, é necessário inserir a tag para o webhook.
O padrão utilizado é ```lts- + <tag>```

Exemplo: **lts-0.0.1**

```
$ docker build . -t db:*tag*
```

## Run

```
$ docker run -d -e MYSQL_DATABASE='demo' -e MYSQL_ALLOW_EMPTY_PASSWORD='yes' --name backend db:*tag*
```

## Logs

```
$ docker logs backend -f
```

## Testar a conexão com o banco de dados

```
$ docker exec -ti backend mysql -u root -p
```
