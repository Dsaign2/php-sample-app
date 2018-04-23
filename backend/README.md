## Build

To build the project, it's needed to insert a tag to the webhook service.
The pattern used is ```lts-*tag*```

E.g.: **lts-0.0.1**

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

## Test connection with database

```
$ docker exec -ti backend mysql -u root -p
```
