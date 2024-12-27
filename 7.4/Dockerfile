FROM mileschou/composer:7.4

RUN apk --no-cache add pcre-dev ${PHPIZE_DEPS} \
      && apk --no-cache add libmcrypt-dev \
      && pecl install mcrypt-1.0.3 \
      && docker-php-ext-enable mcrypt \
      && apk del pcre-dev ${PHPIZE_DEPS}
