FROM ruby:3.2.2

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs

RUN mkdir /v7-0
WORKDIR /v7-0

ADD Gemfile /v7-0/Gemfile
ADD Gemfile.lock /v7-0/Gemfile.lock

RUN bundle install
ADD . /v7-0
