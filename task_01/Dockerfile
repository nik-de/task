FROM centos:centos7

RUN yum install -y wget openssl &&\
    yum -y autoremove &&\
    yum clean all &&\
    wget http://nginx.org/packages/centos/7/x86_64/RPMS/nginx-1.20.1-1.el7.ngx.x86_64.rpm &&\
    rpm -iv nginx-1.20.1-1.el7.ngx.x86_64.rpm

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]