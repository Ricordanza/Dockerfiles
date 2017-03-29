FROM ricordanza/ruby

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
    rbenv install 2.4.1 && \
    rbenv global 2.4.1 && \
    rbenv rehash && \
    gem install serverspec && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
