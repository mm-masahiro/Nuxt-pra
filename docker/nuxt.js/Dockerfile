FROM node:latest

RUN apt-get update && apt-get install -y

WORKDIR /root

RUN npm install yarn

RUN npm install --global @vue/cli @vue/cli-init

EXPOSE 8090

ADD src /src

WORKDIR /src/app
