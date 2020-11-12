FROM rex

MAINTAINER kurgan231@gmail.com

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -q -y wget \
	python3-pip python3-dev  \
	gnupg \
	&& mkdir /tmp/odoo_others \
	&& wget https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.bionic_amd64.deb -P /tmp/odoo_others \
	&& apt install -q -y /tmp/odoo_others/wkhtmltox_0.12.5-1.bionic_amd64.deb \
	&& cd /tmp/odoo_others \
	&& wget -O - https://nightly.odoo.com/odoo.key | apt-key add - \
	&& echo "deb http://nightly.odoo.com/13.0/nightly/deb/ ./" | tee -a /etc/apt/sources.list.d/odoo.list \
	&& apt-get update && apt-get install -q -y odoo \
	&& rm -rf /var/cache/apt \
	&& rm -rf /var/lib/apt/lists \
	&& rm -rf /tmp/odoo_others \
	&& rm -rf /etc/apt/sources.list.d/odoo.list \
	&& apt-key del '5D13 4C92 4CB0 6330 DCEF  E2A1 DEF2 A219 8183 CBB5'
