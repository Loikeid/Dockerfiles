FROM jdk:16

RUN mkdir -p /home/minecraft && mkdir -p /usr/bin/minecraft/libraries

COPY libraries /usr/bin/minecraft/libraries

COPY . /home/minecraft

WORKDIR /home/minecraft

RUN cp server_config/* . && rm -r libraries server_config && rm Dockerfile

VOLUME ["/home/minecraft", "/home/minecraft/mods", "/home/minecraft/config", "/home/minecraft/logs", "/home/minecraft/world"]

EXPOSE 25565/tcp

ENTRYPOINT ["/bin/bash", "run.sh"]
