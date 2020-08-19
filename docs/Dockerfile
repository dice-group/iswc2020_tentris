FROM ruby AS builder


WORKDIR /project

ADD Gemfile Gemfile.lock /project/
RUN bundler install

ADD ./ /project
RUN jekyll build


FROM nginx

COPY --from=builder /project/_site/ /usr/share/nginx/html/iswc2020
