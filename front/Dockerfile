# Dockerfile Front
FROM node:14-alpine AS build
WORKDIR /usr/local/app
COPY ./ /usr/local/app
RUN npm install
RUN npm run build

FROM nginx:1.21.4
COPY --from=build /usr/local/app/dist /usr/share/nginx/html 
COPY /nginx.conf /etc/nginx/conf.d/default.conf