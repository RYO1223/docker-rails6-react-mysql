FROM node:slim

RUN mkdir /myapp
WORKDIR /mayapp
COPY package.json yarn.lock ./

RUN yarn install
