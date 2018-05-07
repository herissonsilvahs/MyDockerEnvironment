ARG UID=root
ARG GID=root

FROM php:7.2.5-apache-stretch

ADD apache2/sites-enable/ /etc/apache2/sites-enabled/

RUN a2enmod rewrite

RUN chown -R ${UID}:${GID} /var/www/html

USER ${UID}
