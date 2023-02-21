FROM ubuntu

RUN apt update

RUN apt install -y apache2

RUN apt install -y apache2-utils

RUN apt clean

RUN apt install -y systemctl

RUN systemctl enable apache2

RUN systemctl start apache2

RUN rm -f /etc/apache2/ports.conf
RUN rm -f /etc/apache2/sites-available/000-default.conf
RUN rm -f /etc/apache2/sites-available/default-ssl.conf

COPY site.conf/. /etc/apache2/sites-available/
COPY ports.conf /etc/apache2/ports.conf
COPY site1.com  /var/www/site1.com
COPY site2.com  /var/www/site2.com
COPY site3.com  /var/www/site3.com

RUN a2dissite 000-default.conf
RUN a2ensite site1com.conf
RUN a2ensite site2com.conf
RUN a2ensite site3com.conf

RUN chown -R $USER:$USER /var/www/
RUN chmod -R 755 /var/www

#RUN apache2ctl configtest

#RUN systemctl restart apache2
