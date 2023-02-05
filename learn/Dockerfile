FROM node:lts-alpine

ENV NODE_ENV=production PORT=3000

WORKDIR /usr/src/app

COPY ["package.json", "package-lock.json*", "./"]

RUN npm install && mv node_modules ../

COPY . .

EXPOSE $PORT
#RUN chown -R node /usr/src/app
#USER node
ENTRYPOINT [ "npm", "run" ]
CMD ["start"]
