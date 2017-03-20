FROM java:7-jre
COPY esf_4.1.0_raspberry-pi-2-nn_installer.deb /tmp/
RUN apt-get update && \
    apt-get -y install dos2unix \
	                   telnet && \
    cd /tmp && \
	dpkg -i esf_4.1.0_raspberry-pi-2-nn_installer.deb && \
	rm esf_4.1.0_raspberry-pi-2-nn_installer.deb && \
	apt-get clean && \
	cd /lib/x86_64-linux-gnu && \
	ln -s libudev.so.1 libudev.so.0
CMD /opt/eurotech/esf/bin/start_kura_background.sh && /bin/bash