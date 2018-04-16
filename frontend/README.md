# PHP Front-End

For this app to run correctly, you need to install [Docker](https://www.docker.com/).

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
$ docker run -d -p 80:80 --rm -name front front-php:*tag*
```
