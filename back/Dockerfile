FROM ruby:2.7

# nodejsとmysql-client (default-mysql-client) のインストール
RUN apt-get update -qq && \
  apt-get install -y curl apt-transport-https wget nodejs default-mysql-client

# Yarn のインストール
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
  echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list && \
  apt-get update -qq && \
  apt-get install -y yarn

RUN mkdir /myapp
WORKDIR /myapp
COPY Gemfile* ./

RUN bundle install
