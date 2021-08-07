FROM jdk:16

RUN mkdir -p /home/minecraft && cd /home/minecraft

COPY server.jar /usr/bin/

COPY config/* /home/minecraft/

ENV MINECRAFT_SERVER=/usr/bin/server.jar

WORKDIR /home/minecraft

VOLUME ["/home/minecraft"]

EXPOSE 25565/tcp

ENTRYPOINT ["/bin/bash", "run.sh"]
