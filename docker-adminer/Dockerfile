FROM mikk150/rpi-php:5.6-apache
MAINTAINER luctogno

RUN DEBIAN_FRONTEND=noninteractive apt-get update && apt-get install -y \
  php5-pgsql php5-mysql php5-sqlite php5-mssql \
  wget

# install adminer and default theme
RUN wget http://www.adminer.org/latest.php -O /var/www/html/index.php
RUN wget https://raw.githubusercontent.com/vrana/adminer/master/designs/pappu687/adminer.css -O /var/www/html/adminer.css

EXPOSE 80
CMD ["apache2-foreground"]