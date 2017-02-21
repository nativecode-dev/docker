FROM node:boron-alpine
MAINTAINER "NativeCode Development (support@nativecode.com)"

RUN set -ex \
    && apk update \
    && apk add git livestreamer \
    && mkdir -p /etc/livestreamer \
    && git clone https://github.com/nativecode-dev/livestreamer-watch.git /opt/livestreamer \
;
