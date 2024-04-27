FROM centos:7
WORKDIR /app
COPY . /app

RUN yum -y install epel-release && \
    yum -y install nginx && \
    yum clean all && \
    rm -rf /var/cache/yum

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]