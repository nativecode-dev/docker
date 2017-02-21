FROM node:boron
MAINTAINER "NativeCode Development (support@nativecode.com)"

RUN set -ex \
    && apt update \
    && apt install -y git livestreamer \
    && mkdir -p /etc/livestreamer \
    && mkdir -p /data \
    && git clone https://github.com/nativecode-dev/livestreamer-watch.git /opt/livestreamer \
    && cd /opt/livestreamer \
    && npm install \
    && npm run build \
;

VOLUME /etc/livestreamer
VOLUME /data

WORKDIR /opt/livestreamer
CMD ["npm", "start"]

