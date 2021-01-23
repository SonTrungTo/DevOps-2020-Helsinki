FROM ubuntu:16.04

WORKDIR /mydir

RUN apt-get update \
    && apt-get install -y curl \
    && curl -sL https://deb.nodesource.com/setup_15.x | bash - \
    && apt-get update && apt-get install -y nodejs git \
    && git clone https://github.com/docker-hy/frontend-example-docker . \
    && npm install \
    && npm install -g serve \
    && apt-get purge -y --auto-remove curl git \
    && rm -rf /var/lib/apt/lists/*

ENV API_URL=http://localhost:8000

EXPOSE 5000
CMD [ "npm", "start" ]