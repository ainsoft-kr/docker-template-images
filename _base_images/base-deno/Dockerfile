FROM ghcr.io/ainsoft-kr/templates/base

USER ainsoft
RUN curl -fsSL https://deno.land/x/install/install.sh | sh
ENV DENO_INSTALL="/home/ainsoft/.deno"
ENV PATH="$DENO_INSTALL/bin:$PATH"