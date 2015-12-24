FROM alpine:3.3
MAINTAINER Lee Verberne <lee@blarg.org>

RUN apk add --update ca-certificates znc && rm -rf /var/cache/apk/*

USER znc
CMD ["znc", "--foreground", "--datadir", "/znc"]
