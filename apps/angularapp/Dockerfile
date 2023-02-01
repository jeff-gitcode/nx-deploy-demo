##########################################################################################
FROM node:lts-alpine

WORKDIR /app

COPY ./dist/apps/angularapp .

RUN npm install http-server -g

RUN yarn install

# dependencies that nestjs needs
RUN yarn add reflect-metadata tslib rxjs helmet cache-manager

EXPOSE 4200

CMD ["http-server", "-p", "4200"]

# FROM nginx:alpine

# COPY --from=builder ./dist/apps/angularapp /usr/share/nginx/html

# EXPOSE 80

# docker build -f ./apps/angularapp/Dockerfile . -t angularapp
# docker run -d -p 4200:4200 angularapp