FROM node:alpine

# Create app directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# Install app dependencies
COPY package.json /usr/src/app/

# If you're in China, or you need to change sources, will be set CHANGE_SOURCE to true in .env.

RUN apk add --update \
    python3 \
    python3-dev \
    py3-pip \
    build-base

RUN npm install

# Bundle app source
COPY laravel-echo-server.json /usr/src/app/laravel-echo-server.json

EXPOSE 3000
CMD [ "npm", "start", "--force" ]
