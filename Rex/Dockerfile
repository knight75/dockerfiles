FROM ubuntu

MAINTAINER kurgan231@gmail.com

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update &&  apt-get -q -y install apache \
	&& rm -rf /var/cache/apt \
	&& rm -rf /var/lib/apt/lists \
	&& chmod 650 $HOME/.vimrc \
	&& chown root:root $HOME/.vimrc

