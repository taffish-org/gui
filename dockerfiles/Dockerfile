FROM ghcr.io/taffish-org/debian:12

LABEL maintainer="taffish@163.com"

WORKDIR /root

ENV USER=root

RUN apt-get update && \
    apt-get install -y curl git default-jdk python3-dev python3-websockify \
                       xfce4 tightvncserver xfce4-terminal xvfb x11vnc dbus-x11 && \
    cd / && git clone https://github.com/novnc/noVNC.git && \
    echo 'cd /' >> /root/.bashrc

ENV TAFFISH_ENV=TAFFISH
ENV TAFFISH_NAME=gui
