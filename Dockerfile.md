##### **Static Website Containerization Using Docker:**



**#vim Dockerfile**



FROM ubuntu:16.04



RUN apt-get update -y

RUN apt-get install -y apache2

RUN chown -R www-data:www-data /var/www/



ENV APACHE\_RUN\_USER www-data

ENV APACHE\_RUN\_GROUP www-data

ENV APACHE\_LOG\_DIR /var/log/apache2

ENV APACHE\_LOCK\_DIR /var/lock/apache2

ENV APACHE\_PID\_FILE /var/run/apache2.pid



ADD index.html /var/www/html/

EXPOSE 80

ENTRYPOINT \["/usr/sbin/apache2ctl"]

CMD \["-D", "FOREGROUND"]



