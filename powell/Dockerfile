FROM buzz

MAINTAINER kurgan231@gmail.com

ARG APPDIR=$DIR
ARG USR=$USER
ARG GRP=$GROUP
WORKDIR $APPDIR
COPY requirements.txt $APPDIR/requirements.txt
COPY entrypoint.sh /entrypoint.sh

RUN addgroup --system $GRP \
	&& adduser --system $USR \
	&& adduser $USR $GRP \
	&& python3 -m venv $APPDIR \
	&& . $APPDIR/bin/activate \ 
	&& pip3 install -r requirements.txt \
	&& chown -R $USR $APPDIR \
	&& chmod +x /entrypoint.sh

USER $USR
ENTRYPOINT ["/entrypoint.sh"]
