FROM httpd

RUN sudo apt update

RUN mkdir /var/www

RUN rm -f /etc/httpd/conf/httpd.conf

COPY httpd.conf /etc/httpd/conf/httpd.conf
COPY site1.com  /var/www/site1.com
COPY site2.com  /var/www/site2.com
COPY site3.com  /var/www/site3.com

RUN chown httpd:httpd -R /var/www/
