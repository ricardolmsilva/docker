FROM node:10-alpine

ENV PORT 3000

# Create app directory
RUN mkdir -p /home/node/app/node_modules 
RUN mkdir -p /home/node/app/.next
RUN chown -R node:node /home/node/app

WORKDIR /home/node/app

COPY package*.json ./

USER node

RUN yarn

COPY --chown=node:node . .

# Building app
EXPOSE 3000

# Running the app
CMD [ "yarn", "dev"]