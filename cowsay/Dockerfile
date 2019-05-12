# Description: This dockerfile uses the centos image
# Version：    V1.0
# Author：     LiLe
# Contact:     836217653@qq.com
# Command：    docker build -t test/cowsay-dockerfile .


FROM docker.io/centos
MAINTAINER LiLe

#install some base command
#install node
#install cowsay

RUN yum -y install wget \
    && wget https://nodejs.org/dist/v8.12.0/node-v8.12.0-linux-x64.tar.xz \
    && xz -d node-v8.12.0-linux-x64.tar.xz \
    && tar -xf node-v8.12.0-linux-x64.tar \
    && ln -s /node-v8.12.0-linux-x64/bin/node /usr/local/bin/node \
    && ln -s /node-v8.12.0-linux-x64/bin/npm /usr/local/bin/npm \
    && npm install -g cowsay \
    && ln -s  /node-v8.12.0-linux-x64/bin/cowsay /usr/local/bin/cowsay \
    && wget http://mirror.centos.org/centos/7/os/x86_64/Packages/recode-3.6-38.el7.x86_64.rpm \
    && rpm -i /recode-3.6-38.el7.x86_64.rpm \
    && wget http://springdale.math.ias.edu/data/puias/7/x86_64/os/Addons/Packages/fortune-mod-1.99.1-17.sdl7.x86_64.rpm \
    && rpm -i /fortune-mod-1.99.1-17.sdl7.x86_64.rpm

CMD fortune -a | cowsay
