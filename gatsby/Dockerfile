FROM ghcr.io/ainsoft-kr/docker-template-images/templates/base-nodejs

RUN cd /home/ainsoft && rm -rf project && npx gatsby new project
COPY --chown=ainsoft ./workspace/anyfiddle.json /home/ainsoft/project/anyfiddle.json