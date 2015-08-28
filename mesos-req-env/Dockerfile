FROM xdevelsistemas/centos-env:node-env
MAINTAINER Clayton Santos da Silva <clayton@xdevel.com.br>

#install mesos
RUN rpm -i http://repos.mesosphere.io/el/7/noarch/RPMS/mesosphere-el-repo-7-1.noarch.rpm && yum -y install mesos-0.23.0
#install java
ENV JDK_VERSION 8u60
ENV JDK_BUILD_VERSION b27
RUN curl -LO "http://download.oracle.com/otn-pub/java/jdk/$JDK_VERSION-$JDK_BUILD_VERSION/jdk-$JDK_VERSION-linux-x64.rpm" -H 'Cookie: oraclelicense=accept-securebackup-cookie' && rpm -i jdk-$JDK_VERSION-linux-x64.rpm; rm -f jdk-$JDK_VERSION-linux-x64.rpm; yum clean all
ENV JAVA_HOME /usr/java/default

#install npm
RUN yum -y install nodejs npm bzip2 gcc gcc-c++ make openssl-devel && \
#install awscli
    yum install -y python-pip git && \
    pip install --upgrade pip && \
    pip install awscli




CMD ["bash"]
