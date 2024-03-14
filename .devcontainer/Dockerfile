FROM ubuntu:22.04

ARG USER_NAME=user1234
ARG UID=21400

RUN apt update && apt -y install --no-install-recommends git sudo rsync python3 gedit openssh-server \
    && rm -rf /var/lib/apt/lists/* && apt-get clean \
    && adduser --disabled-password --gecos '' --shell /bin/bash --uid ${UID} ${USER_NAME} \
    && echo "${USER_NAME} ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers

USER ${USER_NAME}