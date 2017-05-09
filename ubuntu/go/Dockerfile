FROM ricordanza/develop

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
    git clone https://github.com/wfarr/goenv.git ~/.goenv && \
    echo 'export PATH="$HOME/.goenv/bin:$PATH"' >> ~/.bashrc && \
    echo 'eval "$(goenv init -)"' >> ~/.bashrc && \
    export PATH="$HOME/.goenv/bin:$PATH" && \
    eval "$(goenv init -)" && \
    ~/.goenv/bin/goenv install 1.8 && \
    ~/.goenv/bin/goenv global 1.8 && \
    ~/.goenv/bin/goenv rehash && \
    echo "export GOPATH=$HOME/.goenv" >> ~/.bashrc && \
    export GOPATH=$HOME/.goenv && \
    mkdir -p $GOPATH/bin && \
    curl https://glide.sh/get | sh && \
    apt-get autoremove && \
    apt-get autoclean && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
