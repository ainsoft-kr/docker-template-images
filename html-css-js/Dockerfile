FROM ghcr.io/ainsoft-kr/docker-template-images/templates/base-nodejs

USER root

RUN npm install -g serve

USER ainsoft
COPY --chown=ainsoft ./workspace /home/ainsoft/project