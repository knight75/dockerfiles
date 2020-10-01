FROM rex

MAINTAINER kurgan231@gmail.com

ENV DEBIAN_FRONTEND=noninteractive

COPY odoo13.conf /etc/odoo13.conf

RUN apt-get update && apt-get install -q -y wget \
	git python3-pip build-essential python3-dev python3-venv python3-wheel \
	libxslt-dev libzip-dev libldap2-dev libsasl2-dev \
	python3-setuptools node-less libjpeg-dev zlib1g-dev \
	&& useradd -m -d /opt/odoo13 -U -r -s /bin/bash odoo13 \
	&& mkdir -p /opt/odoo13/odoo-custom-addons \
	/tmp/odoo_others \
	&& wget https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.bionic_amd64.deb -P /tmp/odoo_others \
	&& apt install -q -y /tmp/odoo_others/wkhtmltox_0.12.5-1.bionic_amd64.deb \
	&& su - odoo13 \
	&& git clone https://github.com/odoo/odoo --depth 1 --branch 13.0 /opt/odoo13/odoo \
	&& cd /opt/odoo13 \
	&& /bin/bash -c "python3 -m venv odoo-venv && source odoo-venv/bin/activate && pip3 install -r odoo/requirements.txt --no-cache-dir && deactivateé" \
	&& rm -rf /var/cache/apt \
	&& rm -rf /var/lib/apt/lists \
	&& rm -rf /tmp/odoo_others
