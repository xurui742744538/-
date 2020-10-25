# Docker image of dubbo-admin webapp tomcat
# VERSION 0.0.1
# Author: xiaochunping

#基础镜像使用tomcat:7.0.88-jre8
FROM tomcat:7.0.88-jre8

#作者
MAINTAINER xiaochunping <xcp.email@gmail.com>

#定义工作目录
ENV TOMCAT_BASE /usr/local/tomcat


#复制配置文件
#COPY ./server.xml $TOMCAT_BASE/conf/

#复制war包
COPY ./dubbo-consumer.war $TOMCAT_BASE/webapps/

#给配置文件增加读权限
#RUN chmod a+xr $TOMCAT_BASE/conf/server.xml

#删除默认的ROOT文件件
RUN rm -rf $TOMCAT_BASE/webapps/ROOT
