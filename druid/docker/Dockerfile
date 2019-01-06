FROM centos
USER root
EXPOSE 80 22 8088 1947 443 3006 27999 5060 5063 4005
WORKDIR /home/root/druid/
COPY rpms /home/root/druid/
RUN yum install wget -y
RUN wget https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
RUN yum install epel-release-latest-7.noarch.rpm -y
RUN yum install libmicrohttpd-0.9.22-1.el7.centos.x86_64.rpm -y
RUN yum install curl-7.43.0-1.el7.x86_64.rpm libcurl-7.43.0-1.el7.x86_64.rpm -y
RUN yum install sofia-sip-1.12.11-8.fc20.x86_64.rpm -y
RUN yum install raemis-default-4.2-1.CP11.x86_64.VIRTUAL.rpm -y
WORKDIR /home/root/druid/glibc_support/
RUN wget -c http://vault.centos.org/7.5.1804/os/x86_64/Packages/glibc-2.17-222.el7.x86_64.rpm \
    http://vault.centos.org/7.5.1804/os/x86_64/Packages/glibc-common-2.17-222.el7.x86_64.rpm \
    http://vault.centos.org/7.5.1804/os/x86_64/Packages/glibc-2.17-222.el7.i686.rpm
RUN rpm -U --oldpackage *rpm
