FROM ubuntu:17.10

MAINTAINER Arnaud Haas

RUN apt-get update && apt-get install -y apache2
RUN a2enmod proxy_fcgi

ADD app.conf /etc/apache2/sites-available/
RUN a2ensite app

EXPOSE 80

WORKDIR /var/www/html

CMD /usr/sbin/apache2ctl -D FOREGROUND