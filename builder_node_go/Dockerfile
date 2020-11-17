FROM centos:7.6.1810

LABEL MAINTAINER=lyle.lai

ENV GO_VERSION=1.15.5
ENV NODE_VERSION=v14.15.1

# prepare
RUN yum install -y wget &&\
    yum clean all

# install go
RUN wget -P /tmp https://golang.google.cn/dl/go${GO_VERSION}.linux-amd64.tar.gz &&\
    tar -C /usr/local -xzf /tmp/go${GO_VERSION}.linux-amd64.tar.gz &&\
    export PATH=$PATH:/usr/local/go/bin

# install node
RUN wget -P /tmp https://nodejs.org/dist/${NODE_VERSION}/node-${NODE_VERSION}-linux-x64.tar.xz &&\
    tar -C /usr/local -xf /tmp/node-${NODE_VERSION}-linux-x64.tar.xz
