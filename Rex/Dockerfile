FROM ubuntu

MAINTAINER kurgan231@gmail.com

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update &&  apt-get -q -y install postgresql \
	postgresql-contrib \
	&& rm -rf /var/cache/apt \
	&& rm -rf /var/lib/apt/lists
