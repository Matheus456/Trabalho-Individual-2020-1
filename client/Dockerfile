FROM node:14

RUN mkdir -p /app-client
WORKDIR /app-client

COPY package.json /app-client
COPY yarn.lock /app-client

RUN yarn global add @vue/cli@4.4.0
COPY . /app-client

CMD ["yarn", "dev"]
