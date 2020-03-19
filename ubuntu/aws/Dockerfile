FROM ricordanza/python

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
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
    apt-get autoremove && \
    apt-get autoclean && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
