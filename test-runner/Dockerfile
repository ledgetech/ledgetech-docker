FROM openresty/openresty:centos

RUN yum -y install \
    perl-Test-Nginx

RUN adduser http

RUN luarocks install luacov
