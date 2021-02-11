FROM openresty/openresty:1.15.8.3-2-centos

RUN yum -y install \
    perl-Test-Nginx \
    redis

RUN adduser http

RUN luarocks install luacov
