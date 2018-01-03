FROM ubuntu:14.04

RUN apt-get update && apt-get install -y software-properties-common python-software-properties && add-apt-repository -y ppa:dhor/myway && apt-get update && apt-get install -y eos-movrec

# Troque 1000 pelo seu group id, geralmente não precisa alterar nada
RUN export uid=1000 gid=1000 && \
	mkdir -p /home/eos && \
	echo "eos:x:${uid}:${gid}:Eos,,,:/home/eos:/bin/bash" >> /etc/passwd && \
	echo "eos:x:${uid}:" >> /etc/group && \
	echo "eos ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/eos && \
	chmod 0440 /etc/sudoers.d/eos && \
	chown ${uid}:${gid} -R /home/eos

RUN echo "#!/bin/bash \n export QT_X11_NO_MITSHM=1 \n eos_movrec" >> /usr/bin/prof
RUN chmod +x /usr/bin/prof

USER eos
ENV HOME /home/eos
CMD /usr/bin/prof
