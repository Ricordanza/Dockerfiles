FROM ricordanza/develop

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
    git clone https://github.com/wfarr/goenv.git ~/.goenv && \
    echo "export GOPATH=$HOME/.go" >> ~/.bashrc && \
    echo 'export PATH="$HOME/.goenv/bin:$GOPATH/bin:$PATH"' >> ~/.bashrc && \
    echo 'eval "$(goenv init -)"' >> ~/.bashrc && \
    export GOPATH=$HOME/.go && \
    mkdir -p $GOPATH/bin && \
    export PATH="$HOME/.goenv/bin:$GOPATH/bin:$PATH" && \
    eval "$(goenv init -)" && \
    $HOME/.goenv/bin/goenv install 1.13.8 && \
    $HOME/.goenv/bin/goenv global 1.13.8 && \
    $HOME/.goenv/bin/goenv rehash && \
    $HOME/.goenv/shims/go get -u github.com/golang/dep/cmd/dep && \
    apt-get autoremove && \
    apt-get autoclean && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
