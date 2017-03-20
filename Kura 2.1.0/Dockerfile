FROM java:7-jre
RUN apt-get update && \
    apt-get -y install dos2unix \
	                   telnet && \
    cd /tmp && \
	wget http://ftp-stud.fht-esslingen.de/pub/Mirrors/eclipse/kura/releases/2.1.0/kura_2.1.0_raspberry-pi-nn_installer.deb && \
	dpkg -i kura_2.1.0_raspberry-pi-nn_installer.deb && \
	rm kura_2.1.0_raspberry-pi-nn_installer.deb && \
	apt-get clean && \
	cd /lib/x86_64-linux-gnu && \
	ln -s libudev.so.1 libudev.so.0 && \
	mkdir /opt/eclipse/kura/security
CMD /opt/eclipse/kura/bin/start_kura_background.sh && /bin/bash