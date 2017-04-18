FROM ricordanza/python

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
    pip install awscli && \
    apt-get autoremove && \
    apt-get autoclean && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
