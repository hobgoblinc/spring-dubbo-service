from centos:latest

ADD jdk-8u111-linux-x64.tar.gz /usr/java/

ADD spring-dubbo-elasticjob-1.0-SNAPSHOT-prod.tar.gz /usr/dubbo-server/spring-dubbo-elasticjob/

#RUN yum install -y dos2unix && dos2unix /usr/dubbo-server/spring-dubbo-elasticjob/startup.sh

RUN cd /usr/dubbo-server/spring-dubbo-elasticjob/ && sed -i 's/java/\/usr\/java\/jdk1.8.0_111\/bin\/java/g' startup.sh startupd.sh && chmod 777 startup.sh startupd.sh

ENTRYPOINT cd /usr/dubbo-server/spring-dubbo-elasticjob/ && sh startupd.sh