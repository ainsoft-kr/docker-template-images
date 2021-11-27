FROM ghcr.io/ainsoft/templates/base

USER root

RUN apt-get update && apt-get install -y \
	default-jdk \
	&& rm -rf /var/lib/apt/lists/*

USER ainsoft
