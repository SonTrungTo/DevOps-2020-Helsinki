FROM node:alpine

WORKDIR /mydir

RUN apk update \
    && apk add --no-cache curl \
    && curl -sL https://deb.nodesource.com/setup_15.x \
    && apk update && apk add --no-cache git \
    && git clone https://github.com/docker-hy/frontend-example-docker . \
    && npm install \
    && npm install -g serve \
    && apk del curl git \
    && deluser --remove-home node \
    && addgroup -S node -g 9995 \
    && adduser -S -G node -u 9995 node \
    && chown -R node .

USER node

ENV API_URL=http://localhost:8000

EXPOSE 5000
CMD [ "npm", "start" ]