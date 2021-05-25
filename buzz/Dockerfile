FROM ubuntu

MAINTAINER kurgan231@gmail.com

ENV TZ=Europe/Paris
ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update &&  apt-get -q -y install tzdata \
	python3 \
	python3-pip \
	python3-venv \
	&& unlink /etc/localtime \
	&& ln -snf /usr/share/zoneinfo/$TZ /etc/localtime \
	&& echo $TZ > /etc/timezone \
	&& rm -rf /var/cache/apt \
	&& rm -rf /var/lib/apt/lists

