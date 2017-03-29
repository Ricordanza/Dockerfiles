FROM ricordanza/japanize

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
    apt-get install -y --force-yes build-essential curl git zlib1g-dev libssl-dev libreadline-dev libyaml-dev libxml2-dev libxslt-dev && \
    git clone https://github.com/sstephenson/rbenv.git ~/.rbenv && \
    git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build && \
    PATH /root/.rbenv/bin:$PATH && \
    echo 'eval "$(rbenv init -)"' >> /etc/profile.d/rbenv.sh # or /etc/profile && \
    echo 'eval "$(rbenv init -)"' >> .bashrc && \
    rbenv install 2.4.1 && \
    rbenv global 2.4.1 && \
    rbenv rehash && \
    apt-get autoremove && \
    apt-get autoclean && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
