FROM ghcr.io/ainsoft-kr/docker-template-images/templates/base-nodejs

RUN npx create-next-app . --typescript
COPY --chown=ainsoft ./workspace/anyfiddle.json /home/ainsoft/project/anyfiddle.json