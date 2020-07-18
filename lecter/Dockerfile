FROM buzz

MAINTAINER kurgan231@gmail.com

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \ 
	&& apt-get -q -y install openjdk-8-jre \
        && rm -rf /var/cache/apt \
        && rm -rf /var/lib/apt/lists
	&& pip3 install virtualenv \
	tabula-py
