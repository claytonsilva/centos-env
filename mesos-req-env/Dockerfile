FROM xdevelsistemas/centos-env:node-env
MAINTAINER Clayton Santos da Silva <clayton@xdevel.com.br>

#install java
ENV JDK_VERSION 8u60
ENV JDK_BUILD_VERSION b27
RUN curl -LO "http://download.oracle.com/otn-pub/java/jdk/$JDK_VERSION-$JDK_BUILD_VERSION/jdk-$JDK_VERSION-linux-x64.rpm" -H 'Cookie: oraclelicense=accept-securebackup-cookie' && rpm -i jdk-$JDK_VERSION-linux-x64.rpm; rm -f jdk-$JDK_VERSION-linux-x64.rpm; yum clean all
ENV JAVA_HOME /usr/java/default

#install dev tools
RUN yum -y install  unzip  bzip2 gcc gcc-c++ make openssl-devel && \
#install awscli
    yum install -y python-pip git && \
    pip install --upgrade pip && \
    pip install awscli
RUN wget -c http://www.scala-lang.org/files/archive/scala-2.11.8.rpm && \ 
	rpm -ivh scala-2.11.8.rpm && \ 
    wget -c http://ftp.unicamp.br/pub/apache/spark/spark-1.6.1/spark-1.6.1-bin-hadoop2.6.tgz && \
    tar xvf spark-1.6.1-bin-hadoop2.6.tgz  && mv spark-1.6.1-bin-hadoop2.6 /usr/local 

ENV PATH=$PATH:/usr/local/spark-1.6.1-bin-hadoop2.6/bin
