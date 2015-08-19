FROM ubuntu:14.04
MAINTAINER Alan Guo Xiang Tan "https://twitter.com/tgx_world"

RUN apt-get update
RUN apt-get install -y autoconf bison build-essential libssl-dev libyaml-dev libreadline6-dev zlib1g-dev libncurses5-dev git curl libtool libxslt-dev libxml2-dev libpq-dev gawk curl pngcrush python-software-properties software-properties-common tasksel apache2-utils postgresql-client libffi-dev default-jdk make

RUN git clone --depth 1 https://github.com/sstephenson/rbenv.git /root/.rbenv
RUN git clone --depth 1 https://github.com/sstephenson/ruby-build.git /root/.rbenv/plugins/ruby-build
RUN ./root/.rbenv/plugins/ruby-build/install.sh
ENV PATH /root/.rbenv/bin:$PATH
RUN echo 'eval "$(rbenv init -)"' >> /etc/profile.d/rbenv.sh # or /etc/profile
RUN echo 'eval "$(rbenv init -)"' >> ~/.bashrc

# Install lastest versions of JRuby
RUN rbenv install jruby-1.7.19 && \
    rbenv install jruby-1.7.20 && \
    rbenv install jruby-1.7.20.1 && \
    rbenv install jruby-1.7.21 && \
    rbenv install jruby-9.0.0.0
