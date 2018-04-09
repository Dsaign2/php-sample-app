FROM php:7.2-apache

# Enable mysqli to connect to database
RUN docker-php-ext-install mysqli

# Create app directory
WORKDIR /var/www/html/

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY . .