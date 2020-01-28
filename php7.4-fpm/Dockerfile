FROM laradock/php-fpm:latest-7.4

ENV DEBIAN_FRONTEND noninteractive
ENV PATH=$PATH:~/.composer/vendor/bin

RUN set -eux; \
    apt-get update; \
    apt-get upgrade -y; \
    apt-get install -yqq unzip git; \
    rm -rf /var/lib/apt/lists/*

RUN set -eux; \
    curl -sSL https://getcomposer.org/installer | php && mv composer.phar /usr/local/bin/composer; \
    composer global require friendsofphp/php-cs-fixer

