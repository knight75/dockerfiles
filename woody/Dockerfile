FROM ubuntu

MAINTAINER kurgan231@gmail.com

ENV DEBIAN_FRONTEND=noninteractive


RUN apt-get update &&  apt-get -q -y install python3-pip \
	vim \
	&& pip3 install numpy \
	&& pip3 install pandas \
	&& rm -rf /var/cache/apt
