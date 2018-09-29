FROM alpine

LABEL maintainer="ibohonos"

RUN apk update -y 

#DEPENDENCIES
RUN apk add vim

ENTRYPOINT vim

###### CHECK ######
# docker build -t vim ./
# docker run --rm -it vim
