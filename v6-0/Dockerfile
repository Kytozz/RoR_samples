FROM ruby:3.2.2

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs

RUN mkdir /v6-0
WORKDIR /v6-0

ADD Gemfile /v6-0/Gemfile
ADD Gemfile.lock /v6-0/Gemfile.lock

RUN bundle install
ADD . /v6-0
