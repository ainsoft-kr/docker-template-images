FROM ubuntu:21.04

ARG DEBIAN_FRONTEND=noninteractive
ENV TZ=Etc/UTC

RUN apt-get update && apt-get install -y \
	curl \
	build-essential \
	dumb-init \
	git \
	htop \
	less \
	locales \
	nano \
	net-tools \
	openssl \
	software-properties-common \
	sudo \
	unzip \
	vim \
	wget \
	&& rm -rf /var/lib/apt/lists/*

RUN locale-gen en_US.UTF-8
# We cannot use update-locale because docker will not use the env variables
# configured in /etc/default/locale so we need to set it manually.
ENV LC_ALL=en_US.UTF-8 \
	SHELL=/bin/bash

RUN adduser --gecos '' --disabled-password ainsoft && \
	echo "ainsoft ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers.d/nopasswd

RUN curl -SsL https://github.com/boxboat/fixuid/releases/download/v0.4/fixuid-0.4-linux-amd64.tar.gz | tar -C /usr/local/bin -xzf - && \
  chown root:root /usr/local/bin/fixuid && \
  chmod 4755 /usr/local/bin/fixuid && \
  mkdir -p /etc/fixuid && \
  printf "user: ainsoft\ngroup: ainsoft\n" > /etc/fixuid/config.yml

USER ainsoft

COPY ./.bashrc /home/ainsoft/.bashrc


# Create first so these directories will be owned by ainsoft instead of root
# (workdir and mounting appear to both default to root).
RUN mkdir -p /home/ainsoft/project
WORKDIR /home/ainsoft/project
ENV WORKSPACE_DIR=/home/ainsoft/project

ENTRYPOINT ["dumb-init", "fixuid", "-q"]
CMD ["bash"]
