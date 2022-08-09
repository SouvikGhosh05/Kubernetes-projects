FROM ubuntu:20.04

ENV DEBIAN_FRONTEND noninteractive
ARG USER=souvik
RUN apt-get update && \
    apt-get install apt-utils -y && \
    apt-get install sudo -y
     
RUN chmod 0660 /etc/shadow
RUN useradd -u 1500 "$USER" --create-home --user-group
RUN groupmod -g 2000 "$USER"
RUN useradd -u 3000 demo
WORKDIR /home/$USER
