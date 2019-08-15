FROM golang:1.12.8

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
    apt-get install -y curl && \
    apt-get install -y vim && \
    apt-get install -y python3-dev python3-pip && \
    /usr/bin/pip3 install awscli && \
    ln -fs /usr/bin/pip3 /usr/bin/pip && \
    ln -fs /usr/bin/python3 /usr/bin/python && \
    go get -u github.com/golang/dep/cmd/dep && \
    apt-get autoremove -y && \
    apt-get autoclean -y && \
    apt-get clean -y && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
