FROM ghcr.io/ainsoft-kr/docker-template-images/templates/base-python3

ENV PATH="/home/ainsoft/.local/bin:${PATH}"
RUN pip3 install django

RUN django-admin startproject mainsite . && python manage.py migrate

COPY --chown=ainsoft ./workspace/anyfiddle.json /home/ainsoft/project/anyfiddle.json
COPY --chown=ainsoft ./workspace/.gitignore /home/ainsoft/project/.gitignore
COPY --chown=ainsoft ./workspace/mainsite/settings.py /home/ainsoft/project/mainsite/settings.py
