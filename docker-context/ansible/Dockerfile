FROM ubuntu:22.04

RUN apt-get update && \
    apt-get install software-properties-common -y &&\
    add-apt-repository ppa:deadsnakes/ppa -y &&\
    apt-get update &&\
    apt-get install -y python3.10 python3.10-venv

# ssh
RUN apt-get update && \
    apt-get -y install openssh-server \
                       openssh-client \
                       init \
                       docker.io  \
                       apt-transport-https \
                       ca-certificates \
                       curl \
                       gnupg \
                       lsb-release \
                       iptables \
                       vim

RUN sed 's/#PermitRootLogin yes/PermitRootLogin yes/' -i /etc/ssh/sshd_config &&\
    echo 'root:root' | chpasswd

RUN update-alternatives --set iptables /usr/sbin/iptables-legacy && \
    update-alternatives --set ip6tables /usr/sbin/ip6tables-legacy

RUN curl -L https://bootstrap.pypa.io/get-pip.py | python3 && \
    python3 -m pip install ansible
