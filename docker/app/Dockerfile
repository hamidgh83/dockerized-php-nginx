FROM php:8.1-fpm

# Change working directory
WORKDIR /var/www

# Add user for the application
RUN groupadd -g 1000 www
RUN useradd -u 1000 -ms /bin/bash -g www www

# Give permission
RUN chown -R www:www /var/www
RUN chmod -R 777 /var/www

# Change user
USER www

EXPOSE 9000
CMD [ "php-fpm" ]