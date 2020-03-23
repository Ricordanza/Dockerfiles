FROM ricordanza/go

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    curl -L -O https://github.com/tsenart/vegeta/releases/download/v12.8.0/vegeta-12.8.0-linux-amd64.tar.gz && \
    tar xf vegeta-12.8.0-linux-amd64.tar.gz && \
    rm -f vegeta-12.8.0-linux-amd64.tar.gz && \
    chmod +x ./vegeta && \
    mv ./vegeta /usr/bin/ && \
    apt-get autoremove && \
    apt-get autoclean && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
