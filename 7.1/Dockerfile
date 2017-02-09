FROM php:7.1

ENV COMPOSER_HOME /root/.composer
ENV PATH $PATH:$COMPOSER_HOME/vendor/bin
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && \
    apt-get install -y \
        git \
        libpng-dev \
        unzip && \
    docker-php-ext-install gd && \
    pecl install xdebug && \
    echo "zend_extension=/usr/local/lib/php/extensions/no-debug-non-zts-20160303/xdebug.so" > /usr/local/etc/php/conf.d/xdebug.ini && \
    curl -sS https://getcomposer.org/installer | php -- --install-dir=/bin --filename=composer
