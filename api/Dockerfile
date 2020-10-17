FROM node:10-alpine

RUN mkdir -p /home/node/app/node_modules
RUN mkdir -p /home/node/app/.cache
RUN mkdir -p /home/node/app/.temp
RUN mkdir -p /home/node/app/build

RUN chown -R node:node /home/node/app

WORKDIR /home/node/app

COPY package*.json ./

USER node

RUN npm install

COPY --chown=node:node . .

EXPOSE 1337

CMD [ "npm", "run", "develop"]
