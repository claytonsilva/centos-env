FROM centos:7

ENV	LANG en_US.UTF-8
ENV	LC_ALL en_US.UTF-8

# Add EPEL repository
#RUN rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm && \
#    rpm --rebuilddb

RUN yum install -y curl; yum upgrade -y; yum update -y;




CMD ["bash"]
