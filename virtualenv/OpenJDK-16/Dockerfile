CMD ["/bin/bash"]

ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8

RUN apt-get update -y && apt-get install -y wget openjdk-16-jre-headless && rm -rf /var/cache/apt/archives/*

ENV JAVA_VERSION=jdk-16.0.1+9 
