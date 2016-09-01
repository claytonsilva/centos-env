FROM xdevelsistemas/centos-env:latest



#install npm
RUN curl --silent --location https://rpm.nodesource.com/setup_6.x | bash - && yum remove -y nodejs 
RUN     yum -y install nodejs npm bzip2 gcc gcc-c++ make openssl-devel && \
#install awscli
    yum install -y wget git && \
    wget -c https://bootstrap.pypa.io/get-pip.py && \
    python get-pip.py && \
    pip install --upgrade pip && \
    pip install awscli

#latest npm
#RUN npm install --global npm@latest
#install phantomjs + casperjs + bower + grunt-cli +  forever
RUN node -v && \
    npm install -g coffee-script node-gyp && \
    npm install -g phantomjs && \
    npm install -g casperjs && \
    npm install -g bower && \
    npm install -g grunt-cli && \
    npm install -g forever
    npm install -g typescript
    npm install -g typings
    npm install -g gulp-cli

CMD ["bash"]

