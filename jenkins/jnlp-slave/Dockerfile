FROM jenkins/jnlp-slave:3.19-1
MAINTAINER Kai Hu <kay_hu@163.com>

USER root

ADD sources.list /etc/apt/

RUN apt-get update && \
  apt-get install -y apt-transport-https ca-certificates curl gnupg2 software-properties-common && \
  curl -fsSL http://mirrors.aliyun.com/docker-ce/linux/debian/gpg | apt-key add - && \
  add-apt-repository "deb [arch=amd64] http://mirrors.aliyun.com/docker-ce/linux/debian $(lsb_release -cs) stable" && \
  apt-get update && \
  apt-get install -y docker-ce && \
  apt-get clean && \
  usermod -aG docker jenkins

USER jenkins

ENTRYPOINT ["jenkins-slave"]