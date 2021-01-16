FROM ruby:2.6.0

WORKDIR /myapp
RUN apt-get update && apt-get install -y git nodejs
RUN git clone https://github.com/docker-hy/rails-example-project .
RUN gem install bundler
RUN gem install execjs
RUN bundle install
RUN rails db:migrate

EXPOSE 3000
CMD ["rails", "s"]