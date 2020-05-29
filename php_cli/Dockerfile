FROM php:7.3.15-fpm
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install mbstring
RUN apt-get update
RUN apt-get install -y cron

RUN touch /var/log/laravel.log
RUN chmod 0777 /var/log/laravel.log

COPY ./cron/laravel /etc/cron.d/laravel

RUN crontab /etc/cron.d/laravel
CMD ["cron", "-f", "./start.sh"]