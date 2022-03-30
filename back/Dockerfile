# Dockerfile Front
FROM node:17.0-alpine3.14
WORKDIR /usr/src
COPY ./package.json .
RUN npm install 
COPY . .
CMD [ "npm", "run", "start" ]