FROM ricordanza/node

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    npm install -g serverless && \
    pip install awscli && \
    apt-get autoremove && \
    apt-get autoclean && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
