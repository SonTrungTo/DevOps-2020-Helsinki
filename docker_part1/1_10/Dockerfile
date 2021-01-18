FROM ubuntu:16.04

WORKDIR /mydir
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_15.x | bash -
RUN apt-get update && apt-get install -y nodejs git

RUN git clone https://github.com/docker-hy/frontend-example-docker .
RUN npm install
RUN npm install -g serve
ENV API_URL=http://localhost:8000

EXPOSE 5000
CMD [ "npm", "start" ]