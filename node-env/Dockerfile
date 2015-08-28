FROM xdevelsistemas/centos-env:latest



#install npm
RUN yum -y install nodejs npm bzip2 gcc gcc-c++ make openssl-devel && \
#install awscli
    yum install -y python-pip git && \
    pip install --upgrade pip && \
    pip install awscli

#latest npm
RUN npm install --global npm@latest
#install phantomjs + casperjs + bower + grunt-cli +  forever
RUN node -v && \
    npm install -g phantomjs && \
    npm install -g casperjs && \
    npm install -g bower && \
    npm install -g grunt-cli && \
    npm install -g forever

CMD ["bash"]
