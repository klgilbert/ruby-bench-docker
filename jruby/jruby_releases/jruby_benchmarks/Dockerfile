FROM rubybench/jruby_releases_base
MAINTAINER Kasif Gilbert "kasif.gilbert@gmail.com"

RUN git clone --verbose --branch jruby-releases --single-branch https://github.com/klgilbert/ruby-bench-suite.git

ADD runner runner
RUN chmod 755 runner

CMD /bin/bash -l -c "./runner"
