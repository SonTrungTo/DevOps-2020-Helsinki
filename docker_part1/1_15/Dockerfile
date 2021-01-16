FROM ubuntu:latest

WORKDIR /patientor-backend
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y nodejs git curl gnupg1
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
RUN apt-get update && apt-get install -y yarn
RUN git clone https://github.com/SonTrungTo/Fullstack-2020-Helsinki
RUN cp -a ./Fullstack-2020-Helsinki/part9/patientor/backend/. .
RUN rm -rf Fullstack-2020-Helsinki/
RUN yarn
RUN yarn tsc

EXPOSE 3001
CMD [ "yarn", "start" ]