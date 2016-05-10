FROM debian:jessie

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
    apt-get install -y curl && \
    apt-get install -y build-essential && \
    apt-get install -y git && \
    apt-get install -y vim && \
    apt-get install -y python && \    
    apt-get install -y python2.7-dev && \
    curl -kL https://bootstrap.pypa.io/get-pip.py | python && \
    pip install awscli virtualenv virtualenvwrapper lamvery python-lambda-local lambda-controller && \
    echo "WORKON_HOME=~/.virtualenvs" >> ~/.bashrc && \
    echo "source /usr/local/bin/virtualenvwrapper.sh" >> ~/.bashrc && \
    apt-get autoremove && \
    apt-get autoclean && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*