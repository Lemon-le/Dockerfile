FROM docker.io/centos
RUN yum -y install wget
RUN wget https://nodejs.org/dist/v8.12.0/node-v8.12.0-linux-x64.tar.xz
RUN xz -d node-v8.12.0-linux-x64.tar.xz
RUN tar -xf node-v8.12.0-linux-x64.tar
RUN ln -s /node-v8.12.0-linux-x64/bin/node /usr/local/bin/node
RUN ln -s /node-v8.12.0-linux-x64/bin/npm /usr/local/bin/npm 
RUN npm install -g cowsay
RUN ln -s  /node-v8.12.0-linux-x64/bin/cowsay /usr/local/bin/cowsay
RUN wget http://mirror.centos.org/centos/7/os/x86_64/Packages/recode-3.6-38.el7.x86_64.rpm
RUN rpm -i /recode-3.6-38.el7.x86_64.rpm
RUN wget http://springdale.math.ias.edu/data/puias/7/x86_64/os/Addons/Packages/fortune-mod-1.99.1-17.sdl7.x86_64.rpm
RUN rpm -i /fortune-mod-1.99.1-17.sdl7.x86_64.rpm 
