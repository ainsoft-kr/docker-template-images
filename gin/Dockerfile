FROM ghcr.io/ainsoft-kr/docker-template-images/templates/base-golang

RUN go mod init project && go get -u github.com/gin-gonic/gin
COPY --chown=ainsoft ./workspace /home/ainsoft/project
