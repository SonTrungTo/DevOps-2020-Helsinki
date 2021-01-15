FROM ubuntu:16.04

WORKDIR /mydir
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_15.x | bash -
RUN apt-get update && apt-get install -y nodejs git

RUN git clone https://github.com/docker-hy/backend-example-docker .
RUN npm install

EXPOSE 8000