FROM node:18.15 AS build

WORKDIR /usr/local/app

# Compilacion Externa
COPY ./www /usr/local/app/www/

FROM nginx:1.23.2-alpine

COPY --from=build /usr/local/app/www/ /usr/share/nginx/html

EXPOSE 80