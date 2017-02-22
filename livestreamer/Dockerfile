FROM node:boron
MAINTAINER "NativeCode Development (support@nativecode.com)"

USER root
ENV DEBUG "nativecode:*"

RUN set -ex \
    && apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y git python-pip python-dev build-essential \
    && mkdir -p /etc/livestreamer \
    && mkdir -p /data \
    && git clone https://github.com/nativecode-dev/livestreamer-watch.git /opt/livestreamer \
    && cd /opt/livestreamer \
    && npm install \
    && npm run build \
    && pip install --upgrade pip \
    && pip install --upgrade virtualenv \
    && pip install -U livestreamer \
;

VOLUME /etc/livestreamer
VOLUME /data

WORKDIR /opt/livestreamer
CMD ["npm", "start"]

