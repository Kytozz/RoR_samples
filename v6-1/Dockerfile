FROM ruby:3.2.2

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs

RUN mkdir /v6-1
WORKDIR /v6-1

ADD Gemfile /v6-1/Gemfile
ADD Gemfile.lock /v6-1/Gemfile.lock

RUN bundle install
ADD . /v6-1
