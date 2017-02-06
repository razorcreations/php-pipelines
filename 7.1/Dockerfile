FROM php:7.1

ENV COMPOSER_HOME /root/.composer
ENV PATH $PATH:$COMPOSER_HOME/vendor/bin
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && \
    apt-get install -y libpng-dev && \
    docker-php-ext-install gd && \
    curl -sS https://getcomposer.org/installer | php -- --install-dir=/bin --filename=composer
