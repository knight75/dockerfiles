FROM ubuntu

MAINTAINER kurgan231@gmail.com

ENV DEBIAN_FRONTEND=noninteractive
ENV HOME=/root

WORKDIR $HOME

RUN apt-get update &&  apt-get -q -y install python3 \
	python3-pip \
	vim \
	&& rm -rf /var/cache/apt
