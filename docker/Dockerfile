FROM alpine:3.2
MAINTAINER Lee Verberne <lee@blarg.org>

RUN apk add --update \
	ca-certificates \
	znc \
	g++ \
	git \
	make \
	openssl-dev \
	znc-dev \
&& git clone https://github.com/jreese/znc-push.git /root/znc-push \
&& cd /root/znc-push && make && cp push.so /usr/lib/znc \
&& apk del --purge \
	g++ \
	git \
	make \
	openssl-dev \
	znc-dev \
&& rm -rf /var/cache/apk/* /root/znc-push

USER znc
CMD ["znc", "--foreground", "--datadir", "/znc"]
