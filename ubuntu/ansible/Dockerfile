FROM ricordanza/aws

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
    ~/.pyenv/bin/pyenv global system && \
    ~/.pyenv/bin/pyenv rehash && \
    apt-get -y install python-dev libffi-dev libssl-dev && \
    pip install awscli && \
    pip install ansible && \
    apt-get autoremove && \
    apt-get autoclean && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
