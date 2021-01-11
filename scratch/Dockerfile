FROM scratch
ADD rootfs /
RUN apt-get remove --purge --allow-remove-essential -y openssh-server \
	openssh-client \
	perl \
	python3 \
	cryptsetup \
	wget \
	curl \
	ca-certificates \
	perl-modules-5.30 \	
	lxd-installer \
	cryptsetup-bin \
	sound-theme-freedesktop \
	lxd-agent-loader \
&& apt-get autoremove -y \
&& rm -rf /var/cache/apt \
&& rm -rf /var/lib/apt/lists
