#+++++++++++++++++++++++++++++++++++++++
# Dockerfile for webdevops/hhvm-nginx:ubuntu-16.04
#    -- automatically generated  --
#+++++++++++++++++++++++++++++++++++++++

FROM webdevops/hhvm:ubuntu-16.04

MAINTAINER info@webdevops.io
LABEL vendor=WebDevOps.io
LABEL io.webdevops.layout=8
LABEL io.webdevops.version=1.1.4

ENV WEB_DOCUMENT_ROOT  /app
ENV WEB_DOCUMENT_INDEX index.php
ENV WEB_ALIAS_DOMAIN   *.vm
ENV WEB_PHP_SOCKET  127.0.0.1:9000

COPY conf/ /opt/docker/

# Install nginx
RUN /usr/local/bin/apt-install \
        nginx \
    && /opt/docker/bin/provision run --tag bootstrap --role webdevops-nginx --role webdevops-hhvm-nginx \
    && /opt/docker/bin/bootstrap.sh


EXPOSE 80 443
