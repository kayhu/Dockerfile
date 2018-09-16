FROM kayhu/base:jdk8u92
MAINTAINER Kai Hu <kay_hu@163.com>

RUN wget -P download https://services.gradle.org/distributions/gradle-4.6-bin.zip && \
  unzip ./download/gradle-4.6-bin.zip -d /usr/local && \
  rm -rf ./download && \
  ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

ENV GRADLE_HOME /usr/local/gradle-4.6
ENV PATH $GRADLE_HOME/bin:$PATH