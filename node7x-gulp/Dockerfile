FROM ubuntu:16.04

LABEL AUTHOR="Yogesh Linganna"

WORKDIR /opt

ADD setup_7.x /tmp/setup_7.x
RUN bash /tmp/setup_7.x

RUN apt-get update
RUN apt-get install -y build-essential
RUN apt-get install -y nodejs
RUN /usr/bin/npm install -g gulp
RUN /usr/bin/npm install -g bower
RUN apt-get install -y git
RUN /usr/bin/npm install -g gulp-sass@2.3.2

VOLUME ["/opt"]
CMD ["npm", "start"]
