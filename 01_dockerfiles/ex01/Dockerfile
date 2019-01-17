FROM debian

ENV TS3SERVER_LICENSE=accept

WORKDIR /home/teamspeak

RUN apt-get update && apt-get install -y wget bzip2
RUN wget http://dl.4players.de/ts/releases/3.3.0/teamspeak3-server_linux_amd64-3.3.0.tar.bz2
RUN tar xvfj teamspeak3-server_linux_amd64-3.3.0.tar.bz2

EXPOSE 9987/udp 30033 10011

WORKDIR teamspeak3-server_linux_amd64

ENTRYPOINT sh ts3server_minimal_runscript.sh

# docker build -t ex01 .
# docker run -p 9987:9987/udp -p 10011:10011 -p 30033:30033 -e TS3SERVER_LICENSE=accept -ti user
