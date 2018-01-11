FROM ricordanza/japanize

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
    apt-get install -y tmux curl zip vim git git-flow && \
    git clone https://github.com/riywo/anyenv ~/.anyenv && \
    echo "export PATH="$HOME/.anyenv/bin:$PATH"" >> ~/.bashrc && \
    echo 'eval "$(anyenv init -)"' >> ~/.bashrc && \
    apt-get autoremove && \
    apt-get autoclean && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
