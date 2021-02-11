FROM openresty/openresty:1.19.3.1-2-centos

RUN dnf -y install \
    epel-release

RUN dnf -y --enablerepo=powertools install \
    readline-devel \
    git \
    perl-Test-Nginx \
    redis

RUN dnf -y groupinstall "Development Tools"

RUN curl -R -O https://www.lua.org/ftp/lua-5.1.5.tar.gz; \
  tar zxf lua-5.1.5.tar.gz; \
  cd lua-5.1.5; \
  make linux; \
  make install

RUN adduser http

RUN luarocks install luacov; \
    luarocks install lua-resty-redis-connector; \
    luarocks install lua-resty-http; \
    luarocks install lua-resty-qless; \
    luarocks install lua-resty-cookie; \
    luarocks install lua-ffi-zlib
