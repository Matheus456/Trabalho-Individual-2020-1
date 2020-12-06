
FROM node:latest

RUN mkdir -p /client-app

WORKDIR /client-app

COPY package.json /client-app

COPY yarn.lock /client-app

RUN yarn

COPY . /client-app

CMD ["yarn", "dev"]