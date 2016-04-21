#+++++++++++++++++++++++++++++++++++++++
# Dockerfile for webdevops/php-dev:ubuntu-12.04
#    -- automatically generated  --
#+++++++++++++++++++++++++++++++++++++++

FROM webdevops/php:ubuntu-12.04

MAINTAINER info@webdevops.io
LABEL vendor=WebDevOps.io
LABEL io.webdevops.layout=6
LABEL io.webdevops.version=0.23.0

COPY conf/ /opt/docker/

# Install tools
RUN /usr/local/bin/apt-install \
        graphviz \
    && /opt/docker/bin/provision-run.sh webdevops-nginx \
    && /opt/docker/bin/bootstrap.sh
