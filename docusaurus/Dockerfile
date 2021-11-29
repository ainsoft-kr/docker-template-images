FROM ghcr.io/ainsoft-kr/docker-template-images/templates/base-nodejs

RUN cd /home/ainsoft && rm -rf project && npx @docusaurus/init@latest init project classic
COPY --chown=ainsoft ./workspace/anyfiddle.json /home/ainsoft/project/anyfiddle.json