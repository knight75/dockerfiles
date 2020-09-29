FROM lenny

MAINTAINER kurgan231@gmail.com

COPY .apachedir /etc/apache2/ssl/
COPY erp.rfeve.conf /etc/apache2/sites-available

RUN a2enmod proxy proxy_http ssl \
	&& a2ensite erp.rfeve.conf

CMD apachectl -D FOREGROUND
