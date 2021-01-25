FROM node:alpine

WORKDIR /mydir

RUN apk update \
    && apk add --no-cache curl \
    && curl -sL https://deb.nodesource.com/setup_15.x \
    && apk add --no-cache git \
    && git clone https://github.com/docker-hy/backend-example-docker . \
    && npm install \
    && apk del curl git \
    && deluser --remove-home node \
    && addgroup -S node -g 9995 \
    && adduser -S -G node -u 9995 node \
    && chown -R node .

USER node

ENV FRONT_URL=http://localhost:5000

EXPOSE 8000
CMD [ "npm", "start" ]