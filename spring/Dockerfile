FROM ghcr.io/ainsoft-kr/docker-template-images/templates/base-java

COPY --chown=ainsoft ./workspace /home/ainsoft/project
RUN ./mvnw install
