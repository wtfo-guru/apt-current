FROM ubuntu:focal
LABEL org.opencontainers.image.authors="Quien Sabe <qs5779@mail.com>"
COPY 80-acquire-retries /etc/apt/apt.conf.d/
RUN apt-get update && apt-get -y install apt-transport-https curl ruby rubygems-integration ruby-dev \
  build-essential rsync && apt-get clean && find /var/lib/apt/lists/ /var/lib/apt/lists/partial/ -type f -delete
RUN gem install fpm -v 1.14.1
