# Docker image of dubbo-admin spirng boot
# VERSION 0.0.1
# Author: xiaochunping	

#FROM ，表示使用 Jdk8 环境 为基础镜像，如果镜像不是本地的会从 DockerHub 进行下载
FROM openjdk:8-jdk-alpine

#作者
MAINTAINER xiaochunping <xcp.email@gmail.com>

#VOLUME ，VOLUME 指向了一个/tmp的目录，由于Spring Boot使用内置的Tomcat容器，
#Tomcat 默认使用/tmp作为工作目录。这个命令的效果是：在宿主机的/var/lib/docker目录下创建一个临时文件并把它链接到容器中的/tmp目录
VOLUME /tmp

#ADD ，拷贝文件并且重命名
ADD dubbo-admin-0.0.1-SNAPSHOT.jar app.jar

#ENTRYPOINT ，为了缩短 Tomcat 的启动时间，添加java.security.egd的系统属性指向/dev/urandom作为 ENTRYPOINT
ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "-jar", "/app.jar" ]