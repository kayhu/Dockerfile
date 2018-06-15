FROM kayhu/base:jdk8u92
MAINTAINER Kai Hu <kay_hu@163.com>

RUN wget -P download https://services.gradle.org/distributions/gradle-2.14.1-bin.zip && \
  wget -P download http://mirrors.shu.edu.cn/apache/tomcat/tomcat-8/v8.5.31/bin/apache-tomcat-8.5.31.tar.gz && \
  unzip ./download/gradle-2.14.1-bin.zip -d /usr/local && \
  tar -xvf ./download/apache-tomcat-8.5.31.tar.gz -C /usr/local && \
  rm -rf ./download && \
  ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

ENV CATALINA_HOME /usr/local/apache-tomcat-8.5.31
ENV GRADLE_HOME /usr/local/gradle-2.14.1
ENV PATH $CATALINA_HOME/bin:$GRADLE_HOME/bin:$PATH

WORKDIR $CATALINA_HOME

ADD context.xml $CATALINA_HOME/conf/

EXPOSE 8080
CMD ["catalina.sh", "run"]