FROM node:onbuild

RUN useradd --user-group --create-home --shell /bin/false app

ENV HOME=/home/app

COPY package.json $HOME/app/
RUN chown -R app:app $HOME/*

USER app
WORKDIR $HOME/app

RUN npm install
#CMD ["node", "."]
