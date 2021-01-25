FROM node:alpine as build-stage

WORKDIR /usr/src/app

RUN apk update \
    && apk add --no-cache curl \
    && curl -sL https://deb.nodesource.com/setup_15.x \
    && apk add --no-cache git \
    && git clone https://github.com/docker-hy/backend-example-docker . \
    && npm install \
    && npm run build \
    && apk del curl git npm \
    && deluser --remove-home node \
    && addgroup -S app -g 9996 \
    && adduser -S -G app -u 9996 app

ENV FRONT_URL=http://localhost:5000

FROM nginx

COPY --from=build-stage /usr/src/app/dist/ /usr/share/nginx/html