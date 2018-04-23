# PHP App Front-End

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
