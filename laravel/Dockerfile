FROM ghcr.io/ainsoft-kr/docker-template-images/templates/base-php

USER root
RUN apt-get update && apt-get install -y \
    openssl \
    php-bcmath \
    php-ctype \
    php-curl \
    php-fileinfo \
    php-json \
    php-mbstring \
    php-mysql \
    php-xml \
    && rm -rf /var/lib/apt/lists/*

USER ainsoft

RUN composer create-project --prefer-dist laravel/laravel ./
COPY --chown=ainsoft ./workspace/anyfiddle.json /home/ainsoft/project/anyfiddle.json