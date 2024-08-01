FROM node:20-alpine

RUN apk add --no-cache yarn

WORKDIR /docker

COPY package.json yarn.lock /docker/
RUN yarn

COPY . /docker/

RUN yarn run build

ENTRYPOINT [ "yarn", "start:prod" ]