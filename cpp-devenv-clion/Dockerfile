FROM ubuntu:20.04
ARG DEBIAN_FRONTEND=noninteractive

ENV TZ=Asia/Shanghai

RUN apt-get update \
 && apt-get install -y software-properties-common \
 && add-apt-repository -y ppa:ubuntu-toolchain-r/ppa \
 && apt install -y wget build-essential libssl-dev ssh gdb gcc-10 g++-10 clang cmake check rsync tar python \
 && wget -O - https://apt.kitware.com/keys/kitware-archive-latest.asc 2>/dev/null | gpg --dearmor - | tee /etc/apt/trusted.gpg.d/kitware.gpg >/dev/null \
 && apt-add-repository "deb https://apt.kitware.com/ubuntu/ $(lsb_release -cs) main" \
 && apt-get install -y cmake \
 && apt purge -y --auto-remove software-properties-common wget \
 && apt-get clean && mkdir -p /run/sshd

CMD ["/usr/sbin/sshd", "-D"]
