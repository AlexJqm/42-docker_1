FROM ruby

RUN apt-get update && && apt-get upgrade -y
RUN gem install rails

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD RUN bundle install
ONBUILD RUN rails db:migrate
ONBUILD RUN rails db:seed

# docker build -t ex02 .
