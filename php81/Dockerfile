FROM php:8.1-apache AS base

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/
RUN chmod +x /usr/local/bin/install-php-extensions && sync

RUN install-php-extensions gd exif zip pdo_mysql gettext intl mcrypt imagick opcache apcu
RUN a2enmod rewrite headers http2 setenvif ssl
RUN apt-get update && apt-get install imagemagick -y && apt-get clean
RUN a2ensite default-ssl

FROM base as dev

RUN install-php-extensions xdebug
RUN usermod -u 1000 www-data
