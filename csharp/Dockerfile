FROM ghcr.io/ainsoft-kr/docker-template-images/templates/base-csharp

RUN dotnet new console -o .

COPY --chown=ainsoft ./workspace/anyfiddle.json /home/ainsoft/project/anyfiddle.json