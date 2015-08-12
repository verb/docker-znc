FROM alpine:3.2
MAINTAINER Lee Verberne <lee@blarg.org>

RUN apk add --update znc && rm -rf /var/cache/apk/*

USER znc
CMD ["znc", "--foreground", "--datadir", "/etc/znc"]
