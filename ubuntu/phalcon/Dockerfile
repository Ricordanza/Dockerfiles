FROM ricordanza/develop

RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
    apt-get install -y wget software-properties-common && \
    add-apt-repository ppa:ondrej/php && \
    apt-get update -y && \
    apt-get install -y php7.1-common && \
	curl -s https://packagecloud.io/install/repositories/phalcon/stable/script.deb.sh | bash && \
	apt-get install -y php7.1-phalcon && \
	curl -s http://getcomposer.org/installer | php && \


    git clone https://github.com/phalcon/phalcon-devtools.git /opt/phalcon-devtools && \
	ln -fs /opt/phalcon-devtools/phalcon /usr/local/bin/phalcon && \
	chmod +x /usr/local/bin/phalcon && \
	wget https://psysh.org/psysh && \
	chmod +x psysh && \
	curl -sS https://getcomposer.org/installer | php && \
	mv composer.phar /usr/local/bin/composer && \
	mv psysh /usr/local/bin/ && \
    apt-get autoremove && \
    apt-get autoclean && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /var/cache/apt/* && \
    rm -rf /var/log/*
