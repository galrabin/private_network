FROM centos:7.0.1406
USER root
EXPOSE 80
EXPOSE 22
EXPOSE 8088
EXPOSE 1947
EXPOSE 443
EXPOSE 3006
EXPOSE 27999
EXPOSE 5060
EXPOSE 5063
EXPOSE 4005
WORKDIR /home/root/druid/
COPY rpms /home/root/druid/
RUN yum install wget -y
RUN wget https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
RUN yum install epel-release-latest-7.noarch.rpm -y
#RUN yum install libmicrohttpd-0.9.22-1.el7.centos.x86_64.rpm -y
#RUN yum install curl-7.43.0-1.el7.x86_64.rpm libcurl-7.43.0-1.el7.x86_64.rpm -y
#RUN yum install sofia-sip-1.12.11-8.fc20.x86_64.rpm -y
#RUN yum install raemis-default-4.2-1.CP11.x86_64.VIRTUAL.rpm -y
CMD /bin/sh