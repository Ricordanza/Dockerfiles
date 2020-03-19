FROM golang:1.12.8

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
    apt-get install -y curl vim unzip && \
    git clone https://github.com/awslabs/git-secrets.git && \
	cd git-secrets && \
	make install && \
	cd .. && \
	rm -rf git-secretss && \
    curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && \
	unzip awscliv2.zip && \
	./aws/install && \
    rm -f awscliv2.zip && \
    rm -rf ./aws && \
    echo '# aws completer' >> .bashrc && \
    echo "complete -C '/usr/local/bin/aws_completer' aws" >> .bashrc && \
    go get -u github.com/golang/dep/cmd/dep && \
    apt-get autoremove -y && \
    apt-get autoclean -y && \
    apt-get clean -y && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
