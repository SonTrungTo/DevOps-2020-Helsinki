FROM node:alpine as build-stage

ENV API_URL=http://localhost:8000

WORKDIR /usr/src/app/

RUN apk update \
    && apk add --no-cache curl \
    && curl -sL https://deb.nodesource.com/setup_15.x \
    && apk update && apk add --no-cache git \
    && git clone https://github.com/docker-hy/frontend-example-docker . \
    && npm install \
    && npm install -g serve \
    && npm run build \
    && apk del curl git npm \
    && deluser --remove-home node \
    && addgroup -S node -g 9995 \
    && adduser -S -G node -u 9995 node \
    && chown -R node .

USER node

EXPOSE 5000

FROM nginx

COPY --from=build-stage /usr/src/app/dist/ /usr/share/nginx/html