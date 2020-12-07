FROM node:latest

RUN mkdir -p /app-client
WORKDIR /app-client

COPY package.json /app-client
COPY yarn.lock /app-client

RUN yarn

COPY . /app-client

CMD ["yarn", "dev"]
