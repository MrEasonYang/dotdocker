FROM alpine:latest 
MAINTAINER EasonYang <mail@eason-yang.com>

RUN \   
  apk --update --upgrade add \       
  privoxy \   
  && rm /var/cache/apk/*

ENV FORWARD_SOCKS5_ADDRESS 0.0.0.0
ENV FORWARD_SOCKS5_PORT 8095

EXPOSE 8118

ADD privoxy/entrypoint.sh /entrypoint.sh
ADD privoxy/conf /conf

ENTRYPOINT ["/entrypoint.sh"]
