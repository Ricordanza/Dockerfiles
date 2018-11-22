FROM ricordanza/develop

ENV DEBIAN_FRONTEND=noninteractive
RUN rm /bin/sh && ln -s /bin/bash /bin/sh && \
    apt-get update -y && \
	curl -s https://packagecloud.io/install/repositories/phalcon/stable/script.deb.sh | bash && \
	apt-get install -y wget php7.2 php7.2-phalcon && \
	git clone https://github.com/phalcon/phalcon-devtools.git /opt/phalcon-devtools && \
	ln -fs /opt/phalcon-devtools/phalcon.php /usr/local/bin/phalcon && \
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
