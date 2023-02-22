FROM httpd:2.4
RUN mkdir /var/www
RUN mkdir /var/www/site1.com
RUN chown -R $USER:$USER /var/www
RUN chmod -R 755 /var/www
RUN rm -f /usr/local/apache2/conf/httpd.conf
COPY httpd.conf /usr/local/apache2/conf/
COPY index.html /var/www/site1.com/
