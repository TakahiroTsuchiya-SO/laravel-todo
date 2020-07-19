FROM php:7.2-fpm

RUN apt-get update -y

RUN apt-get install -y \
    git \
    vim 
    # pdo_mysql \
    # zip \
    # unzip \
    # libpq-dev \
    # docker-php-ext-install \
    # pdo_pgsql

# install composer
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
RUN php composer-setup.php
RUN php -r "unlink('composer-setup.php');"
RUN mv composer.phar /usr/local/bin/composer  
RUN chmod +x /usr/local/bin/composer

# add alias
RUN echo "" >> ~/.bashrc
RUN echo "alias ll='ls -l'" >> ~/.bashrc

WORKDIR /var/www/html

# FROM php:7.2-fpm
# # install composer
# RUN cd /usr/bin && curl -s http://getcomposer.org/installer | php && ln -s /usr/bin/composer.phar /usr/bin/composer
# RUN apt-get update \
# && apt-get install -y \
# git \
# zip \
# unzip \
# vim
# RUN apt-get update \
#     && apt-get install -y libpq-dev \
#     && docker-php-ext-install pdo_mysql pdo_pgsql
# WORKDIR /var/www/html