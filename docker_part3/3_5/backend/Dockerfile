FROM ubuntu:16.04

WORKDIR /mydir

RUN apt-get update \
    && apt-get install -y curl \
    && curl -sL https://deb.nodesource.com/setup_15.x | bash - \
    && apt-get update && apt-get install -y nodejs git \
    && git clone https://github.com/docker-hy/backend-example-docker . \
    && npm install \
    && rm -rf /var/lib/apt/lists/* \
    && apt-get purge -y --auto-remove curl git \
    && useradd -m mydir

USER mydir

ENV FRONT_URL=http://localhost:5000

EXPOSE 8000
CMD [ "npm", "start" ]