FROM ghcr.io/ainsoft-kr/docker-template-images/templates/base-nodejs

RUN sudo npm install -g @angular/cli
RUN cd /home/ainsoft && rm -rf project && ng new project --defaults
COPY --chown=ainsoft ./workspace/anyfiddle.json /home/ainsoft/project/anyfiddle.json