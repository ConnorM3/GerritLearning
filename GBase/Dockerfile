FROM ubuntu:14.04
USER root
RUN apt-get update && apt-get install -y git default-jdk wget nano
RUN apt-get update
WORKDIR /opt
RUN git clone http://github.com/ConnorM3/GerritLearning.git
