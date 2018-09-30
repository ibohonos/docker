FROM ubuntu:latest

LABEL maintainer="ibohonos"

# prerequisites for valgrind
RUN apt-get update -y
RUN apt-get install -y build-essential valgrind vim nano

WORKDIR /app
CMD /bin/bash

###### CHECK ######
# docker build -t valgrind-image ./
# docker run --rm -it valgrind-image
# valgrind --help