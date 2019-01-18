FROM debian

RUN apt-get update && apt-get upgrade -y && apt-get install -y wget default-jre

WORKDIR server-minecraft

RUN wget	https://launcher.mojang.com/v1/objects/3737db93722a9e39eeada7c27e7aca28b144ffa7/server.jar && \
		java -Xmx1024M -Xms1024M -jar server.jar

RUN echo 'eula=true' > eula.txt

EXPOSE 25565

# docker build -t server-minecraft .
# docker run --rm -d -p 25565:25565 server-minecraft
