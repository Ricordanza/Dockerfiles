FROM ricordanza/node

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
    apt-get install -y python && \
    apt-get install -y python-pip && \
    apt-get install -y python3-pip && \    
    pip install virtualenv virtualenvwrapper ipython && \
    echo "WORKON_HOME=~/.virtualenvs" >> ~/.bashrc && \
    echo "source /usr/local/bin/virtualenvwrapper.sh" >> ~/.bashrc && \
    npm install -g serverless && \
    pip install awscli && \
    apt-get autoremove && \
    apt-get autoclean && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
