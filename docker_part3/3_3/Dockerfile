FROM ubuntu:16.04

WORKDIR /app

RUN apt-get update \
    && apt-get install -y git \
    && git clone https://github.com/SonTrungTo/docker-hy.github.io . \
    && docker build -t 011092295y/docker-hy-course .