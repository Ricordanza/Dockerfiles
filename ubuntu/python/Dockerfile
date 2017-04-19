FROM ricordanza/japanize

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
    apt-get install -y curl zip git vim python python-pip && \
    pip install virtualenv virtualenvwrapper ipython && \
    echo "WORKON_HOME=~/.virtualenvs" >> ~/.bashrc && \
    echo "source /usr/local/bin/virtualenvwrapper.sh" >> ~/.bashrc && \
    git clone https://github.com/yyuu/pyenv.git ~/.pyenv && \
    echo 'export PYENV_ROOT=$HOME/.pyenv' >> ~/.bashrc && \
    echo 'export PATH=$PYENV_ROOT/bin:$PATH' >> ~/.bashrc && \
    echo 'eval "$(pyenv init -)"' >> ~/.bashrc && \
    echo 'eval "$(pyenv init -)"' >> /etc/profile && \
    eval "$(~/.pyenv/bin/pyenv init -)" && \
    apt-get autoremove && \
    apt-get autoclean && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
