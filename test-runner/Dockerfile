FROM openresty/openresty:1.15.8.3-2-centos

RUN yum -y install epel-release

RUN yum -y install \
    git \
    perl-Test-Nginx \
    perl-Digest-SHA \
    redis

RUN adduser http

RUN luarocks install luacov; \
    luarocks install lua-resty-redis-connector; \
    luarocks install lua-resty-http; \
    luarocks install lua-resty-qless; \
    luarocks install lua-resty-cookie; \
    luarocks install lua-ffi-zlib
