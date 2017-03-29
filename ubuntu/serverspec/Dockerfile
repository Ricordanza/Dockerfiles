FROM ricordanza/ruby

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
    gem install serverspec && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
