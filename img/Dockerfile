FROM ubuntu

MAINTAINER Gianluca Damaggio <damaggiogianluca@gmail.com>

RUN apt update && \
apt -y upgrade   

RUN apt-get update && \
apt-get -y install cmake protobuf-compiler && \
apt-get install -y git && \
apt-get install -y build-essential && \
apt-get -y install python3 && \
apt-get -y install python3-dev && \
apt install -y python3-distutils

RUN cd home && \
    mkdir Admin

RUN mkdir /home/Admin/github && \
cd /home/Admin/github && \
git clone https://github.com/Flavia95/VGpop.git  && \
git clone --recursive https://github.com/vgteam/odgi.git && \
cd odgi && \
cmake -H. -Bbuild && \
cmake --build build -- -j 3

WORKDIR /home/Admin/github/odgi
