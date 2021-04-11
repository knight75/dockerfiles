FROM buzz

MAINTAINER kurgan231@gmail.com

WORKDIR /opt/app
COPY requirements.txt /opt/app/requirements.txt

RUN addgroup --system djgroup && adduser --system djuser && adduser djuser djgroup && python3 -m venv /opt/app/ \
&& . /opt/app/bin/activate && pip3 install -r requirements.txt \
&& chown -R djuser /opt/app

USER djuser

