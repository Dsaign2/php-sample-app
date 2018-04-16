FROM php:7.2-apache

# Enable mysqli to connect to database
RUN docker-php-ext-install mysqli

# Create app directory
WORKDIR /var/www/html/

# Copy files from root to workdir
COPY . .
