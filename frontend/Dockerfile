FROM node:slim

RUN mkdir /myapp
WORKDIR /myapp
COPY package.json yarn.lock ./

RUN yarn install
