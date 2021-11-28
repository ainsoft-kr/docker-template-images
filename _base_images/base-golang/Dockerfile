FROM ghcr.io/ainsoft-kr/templates/base

USER root

RUN apt-get update && apt-get install -y \
	golang-go \
	&& rm -rf /var/lib/apt/lists/*

USER ainsoft
ENV GOPATH=/home/ainsoft/.go
RUN mkdir $GOPATH

USER ainsoft