FROM ricordanza/develop

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
    apt-get install -y golang && \
    mkdir -p ~/.go/bin && \
    echo "export GOPATH=$HOME/.go" >> ~/.bashrc && \
    echo "export PATH=$PATH:$GOPATH/bin:/usr/local/go/bin" >> ~/.bashrc && \
    export GOPATH=$HOME/.go && \
    export PATH=$PATH:$GOPATH/bin:/usr/local/go/bin && \
    curl https://glide.sh/get | sh && \
    apt-get autoremove && \
    apt-get autoclean && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
