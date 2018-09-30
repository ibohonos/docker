FROM ubuntu

MAINTAINER ibohonos

RUN apt-get update && apt-get upgrade -y && apt-get install -y nodejs npm git vim nano

RUN npm install yarn --global && npm install npm --global

###### CHECK ######
# docker build -t node-server ./
# docker run --rm -it node-server
