FROM ubuntu

RUN apt update

RUN apt install -y apache2

RUN apt install -y apache2-utils

RUN apt clean

RUN apt install -y systemctl

RUN systemctl enable apache2

RUN systemctl start apache2

RUN rm -f /etc/httpd/conf/httpd.conf

COPY httpd.conf /etc/httpd/conf/httpd.conf
#COPY site1.com  /var/www/site1.com
#COPY site2.com  /var/www/site2.com
#COPY site3.com  /var/www/site3.com

#RUN chown httpd:httpd -R /var/www/
