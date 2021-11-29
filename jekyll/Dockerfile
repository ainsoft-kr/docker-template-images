FROM ghcr.io/ainsoft-kr/docker-template-images/templates/base-ruby

USER root
RUN gem install bundler jekyll
USER anyfiddle

RUN  cd /home/ainsoft && \
    rm -rf project && \
    jekyll new project
COPY --chown=ainsoft ./workspace/anyfiddle.json /home/ainsoft/project/anyfiddle.json