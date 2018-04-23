FROM php:7-apache

RUN ln -s /etc/apache2/mods-available/expires.load /etc/apache2/mods-enabled/
RUN ln -s /etc/apache2/mods-available/rewrite.load /etc/apache2/mods-enabled/
RUN ln -s /etc/apache2/mods-available/headers.load /etc/apache2/mods-enabled/
RUN apt update && apt install --yes --force-yes libpng-dev
RUN docker-php-ext-install -j$(nproc) gd mysqli
RUN chown -R www-data:www-data /var/www/html
RUN chmod -R 774 /var/www/html
EXPOSE 80
