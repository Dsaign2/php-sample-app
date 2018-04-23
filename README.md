# Sistemas para Internet - SecDevOps

***nac:*** Criação de uma aplicação no formato "CRUD" executada em containers com base na linguagem "PHP" e no banco de dados "MySQL";

---

***Importante:***

Instruções sobre modelo de execução e entregáveis podem ser obtidas no [diretório de documentação](https://github.com/fiapsecdevops/php-sample-app/tree/master/docs) ou no portal do aluno;

Duvidas podem ser enviadas para <profhelder.pereira@fiap.com.br>

Esta app foi adaptada do exemplo contido [neste artigo](https://www.tutorialrepublic.com/php-tutorial/php-mysql-crud-application.php)

A estrutura foi criada com base nas seguintes tags:

- frontend-0.1: Versão de testes SEM conexão com o banco para a primeira parte da NAC;
- stable:  Versão COM as linhas de conexão com o banco configuradas, será necessário que o MySQL esteja operante para testes faltando apenas a criação do Dockerfile da aplicação/mysql;



## Build Backend

To build the project, it's needed to insert a tag to the webhook service.<br>
The pattern used is ```prod-*tag*```

E.g.: **prod-0.0.1**

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

# Build Front-End

For this app to run correctly, you first need to install [Docker](https://www.docker.com/)<br>
and open the Docker Quickstart Terminal.

When it's needed to insert a tag, provide it with the pattern ```prod-*tag*```<br>
E.g.: **prod-0.0.1**<br>

Run these commands in order to run the project:

### Clone the repository
```
$ git clone https://github.com/Dsaign2/php-sample-app php-sample-app
$ cd php-sample-app
```

### Build

```
$ cd frontend
$ docker build . -t front-php:*tag*
```

### Run
```
$ docker run -d -p 80:80 --rm --name front front-php:*tag*
```
