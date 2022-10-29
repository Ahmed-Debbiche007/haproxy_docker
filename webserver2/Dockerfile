FROM centos:7.7.1908


RUN yum -y --setopt=tsflags=nodocs install \
    httpd \
    && rm -rf /tmp/* \
    && rm -rf /var/cache/yum/* \
    && rm -rf /run/httpd/* /tmp/httpd* \
    && yum clean all


COPY webserver2/httpd /var/www/html


WORKDIR /var/www/html


EXPOSE 80

CMD [ "/usr/sbin/httpd", "-D", "FOREGROUND" ]
