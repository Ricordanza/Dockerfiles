FROM ricordanza/develop

ENV DEBIAN_FRONTEND=noninteractive
RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
	curl -OL https://julialang-s3.julialang.org/bin/linux/x64/1.3/julia-1.3.1-linux-x86_64.tar.gz && \
    tar -xzf julia-1.3.1-linux-x86_64.tar.gz && \
	mv julia-1.3.1 /usr/share/julia && \
    echo "export PATH=/usr/share/julia/bin:$PATH" >> ~/.bashrc && \
    source ~/.bashrc && \
    rm -rf julia-1.3.1-linux-x86_64.tar.gz && \
    apt-get autoremove && \
    apt-get autoclean && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
