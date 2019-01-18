FROM ubuntu:14.04

ENV DEBIAN_FRONTEND noninteractive

RUN 	apt-get update && \
	apt-get upgrade -y && \
	apt-get install -y curl lib32gcc1

RUN mkdir -p	/opt/steamcmd && \
		cd /opt/steamcmd && \
		curl -s http://media.steampowered.com/installer/steamcmd_linux.tar.gz | tar -vxz

WORKDIR /opt/steamcmd

ENTRYPOINT ["./steamcmd.sh"]
