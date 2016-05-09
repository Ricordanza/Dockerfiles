FROM debian:jessie

RUN apt-get update -y && \
    apt-get install -y curl && \
    apt-get install -y build-essential && \
    apt-get install -y vim && \
    apt-get install -y python && \    
    apt-get install -y python2.7-dev && \
    curl -kL https://bootstrap.pypa.io/get-pip.py | python && \
    pip install aws virtualenv virtualenvwrapper lamvery python-lambda-local lambda-controller && \
    echo "source /usr/local/bin/virtualenvwrapper.sh" >> .bashrc && \
    echo "export WORKON_HOME=$HOME/.virtualenvs" >> .bashrc && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*