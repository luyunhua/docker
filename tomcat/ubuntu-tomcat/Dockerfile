FROM ubuntu:latest
LABEL author="luyunhua1987@gmail.com"

WORKDIR /
# jdk: https://download.oracle.com/otn-pub/java/jdk/8u191-b12/2787e4a523244c269598db4e85c51e0c/jdk-8u191-linux-x64.tar.gz
ADD ./jdk-8u191-linux-x64.tar.gz /

RUN apt-get update \
    && apt-get -y install wget \
    && wget http://mirror.bit.edu.cn/apache/tomcat/tomcat-9/v9.0.13/bin/apache-tomcat-9.0.13.tar.gz \
    && tar zxvf apache-tomcat-9.0.13.tar.gz

ENV JAVA_HOME=/jdk1.8.0_191
ENV PATH=$PATH:/${JAVA_HOME}/bin

CMD ["/apache-tomcat-9.0.13/bin/catalina.sh", "run"]