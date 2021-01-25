FROM node:alpine as build-stage

WORKDIR /usr/src/app

RUN apk update \
    && apk add --no-cache curl \
    && curl -sL https://deb.nodesource.com/setup_15.x \
    && apk add --no-cache git \
    && git clone https://github.com/docker-hy/frontend-example-docker . \
    && npm install \
    && npm install -g serve \
    && npm run build \
    && apk del curl git curl npm \
    && deluser --remove-home node \
    && addgroup -S app -g 9995 \
    && adduser -S -G app -u 9995 app \
    && chown -R app .

USER app

ENV API_URL=http://localhost:8000

FROM nginx

COPY --from=build-stage /usr/src/app/dist/ /usr/share/nginx/html