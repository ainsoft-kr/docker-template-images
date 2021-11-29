FROM ghcr.io/ainsoft-kr/docker-template-images/templates/base-nodejs

RUN cd .. \
    && npm init vite@latest project --template react \
    && cd project \
    && npm install
COPY --chown=ainsoft ./workspace/anyfiddle.json /home/ainsoft/project/anyfiddle.json
COPY --chown=ainsoft ./workspace/vite.config.js /home/ainsoft/project/vite.config.js