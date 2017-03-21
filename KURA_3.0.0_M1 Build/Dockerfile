FROM maven:3-jdk-8
COPY equinox-SDK-Neon.1.zip /root/
RUN apt-get update && \
    apt-get -y install zip && \
	cd /root && \
    git clone -b KURA_3.0.0_M1 https://github.com/eclipse/kura.git && \
	cd kura && \
	sed -i 's/http:\/\/ftp-stud.fht-esslingen.de\/pub\/Mirrors\/eclipse\/equinox\/drops\/R-Neon.1-201609071200/file:\/\/\/root/g' /root/kura/target-platform/p2-repo-equinox_3.11.1/pom.xml && \
	./build-all.sh