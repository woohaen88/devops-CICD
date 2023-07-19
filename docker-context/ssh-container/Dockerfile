# FROM ubuntu:22.04

# RUN apt-get update && \
#     apt-get -y install openssh-server openssh-client init docker.io  apt-transport-https ca-certificates curl gnupg lsb-release iptables vim

# # ssh setting
# RUN sed 's/#PermitRootLogin yes/PermitRootLogin yes/' -i /etc/ssh/sshd_config &&\
#     echo 'root:root' | chpasswd && \
#     service ssh restart

# RUN update-alternatives --set iptables /usr/sbin/iptables-legacy && \
#     update-alternatives --set ip6tables /usr/sbin/ip6tables-legacy


# COPY ./BUILD_Dockerfile /root/Dockerfile

# CMD ["/sbin/init"]

FROM ururu/ssh-container:latest