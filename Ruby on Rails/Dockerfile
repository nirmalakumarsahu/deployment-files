FROM ruby:3.2-alpine

LABEL maintainer="yourname@example.com"

WORKDIR /app

RUN apk add --no-cache build-base postgresql-dev nodejs yarn

COPY Gemfile Gemfile.lock ./

RUN bundle install

COPY . .

EXPOSE 3000

CMD ["rails", "server", "-b", "0.0.0.0"]