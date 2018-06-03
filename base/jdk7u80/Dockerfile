FROM centos:7
MAINTAINER Kai Hu <kay_hu@163.com>

RUN yum install -y net-tools unzip vim wget

ADD jdk-7u80-linux-x64.tar.gz /usr/local

ENV JAVA_HOME /usr/local/jdk1.7.0_80
ENV PATH $JAVA_HOME/bin:$PATH
