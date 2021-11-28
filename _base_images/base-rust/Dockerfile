FROM ghcr.io/ainsoft-kr/docker-template-images/templates/base

RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y --no-modify-path
ENV PATH="/home/ainsoft/.cargo/bin:${PATH}"
ENV USER=ainsoft

