FROM ricordanza/ruby

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    curl https://cli-assets.heroku.com/install-ubuntu.sh | sh && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
