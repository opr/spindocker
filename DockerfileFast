FROM wordpress:latest

RUN apt-get update; \
  apt-get install sudo -y; \
  apt-get install git nano -y; \
  apt-get install iputils-ping -y; \
  apt-get install wget -y; \
  apt-get install unzip -y; \
  apt-get install subversion -y
# install msmtp SMPT client and configure mailhog
RUN apt-get install msmtp -y

RUN pecl install xdebug

RUN echo "html_errors=On" >> /usr/local/etc/php/conf.d/html_errors.ini

RUN docker-php-ext-enable xdebug