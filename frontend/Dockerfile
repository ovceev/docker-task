FROM node:12-alpine
RUN mkdir /app && chown -R node:node /app
USER node
WORKDIR /app
COPY --chown=node:node . /app
RUN npm install --only=prod
CMD npm run start
