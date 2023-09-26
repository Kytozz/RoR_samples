FROM ruby:2.7.8

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs

RUN mkdir /v5-0
WORKDIR /v5-0

ADD Gemfile /v5-0/Gemfile
ADD Gemfile.lock /v5-0/Gemfile.lock

RUN bundle install
ADD . /v5-0
