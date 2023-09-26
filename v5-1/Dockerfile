FROM ruby:2.7.8

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs

RUN mkdir /v5-1
WORKDIR /v5-1

ADD Gemfile /v5-1/Gemfile
ADD Gemfile.lock /v5-1/Gemfile.lock

RUN bundle install
ADD . /v5-1
