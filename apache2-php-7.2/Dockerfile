ARG UID=root
ARG GID=root

FROM php:7.2.5-apache-stretch

RUN apt-get update

RUN apt-get install git -y

ADD apache2/sites-enable/ /etc/apache2/sites-enabled/

RUN a2enmod rewrite

RUN chown -R ${UID}:${GID} /var/www/html

USER ${UID}

RUN php -r "copy('https://getcomposer.org/installer', '/var/www/html/composer-setup.php');"

RUN php /var/www/html/composer-setup.php --install-dir=/usr/bin --filename=composer

RUN php -r "unlink('/var/www/html/composer-setup.php');"
