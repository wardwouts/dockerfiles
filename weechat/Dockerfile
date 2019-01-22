FROM alpine:latest
LABEL maintainer Ward Wouts <ward@wouts.nl>

RUN apk add --no-cache \
	ca-certificates \
	python \
	py2-pip \
	weechat \
	weechat-python \
	weechat-perl

ENV HOME /home/user

RUN adduser -S user \
	&& chown -R user $HOME

WORKDIR $HOME
USER user

ENTRYPOINT [ "weechat" ]
