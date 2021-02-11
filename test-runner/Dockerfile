FROM openresty/openresty:1.17.8.2-5-centos

RUN dnf -y install \
    epel-release

RUN dnf -y --enablerepo=PowerTools install \
    git \
    perl-Test-Nginx \
    redis

RUN adduser http

RUN luarocks install luacov; \
    luarocks install lua-resty-redis-connector; \
    luarocks install lua-resty-http; \
    luarocks install lua-resty-qless; \
    luarocks install lua-resty-cookie; \
    luarocks install lua-ffi-zlib
