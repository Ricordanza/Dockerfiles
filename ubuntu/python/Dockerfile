FROM ricordanza/japanize

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
    apt-get install -y curl && \
    apt-get install -y git && \
    apt-get install -y vim && \
    apt-get install -y python && \
    apt-get install -y python-pip && \
    apt-get install -y python3-pip && \    
    pip install virtualenv virtualenvwrapper ipython && \
    echo "WORKON_HOME=~/.virtualenvs" >> ~/.bashrc && \
    echo "source /usr/local/bin/virtualenvwrapper.sh" >> ~/.bashrc && \
    git clone https://github.com/sstephenson/rbenv.git ~/.rbenv && \
    echo 'export PYENV_ROOT=$HOME/.pyenv' >> ~/.bashrc && \
    echo 'export PATH=$PYENV_ROOT/bin:$PATH' >> ~/.bashrc && \
    echo 'eval "$(pyenv init -)"' >> ~/.bashrc && \
    echo 'eval "$(pyenv init -)"' >> /etc/profile && \
    ~/.pyenv/bin/pyenv install 3.6.1 && \
    ~/.pyenv/bin/pyenv global 3.6.1 && \
    ~/.pyenv/bin/pyenv rehash && \
    apt-get autoremove && \
    apt-get autoclean && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
