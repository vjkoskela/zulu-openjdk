FROM ubuntu:16.04

#
# UTF-8 by default
#
RUN apt-get -qq update
RUN apt-get install locales
RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8

#
# Pull Zulu OpenJDK binaries from official repository:
#
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 0x219BD9C9
RUN echo "deb http://repos.azulsystems.com/ubuntu stable main" >> /etc/apt/sources.list.d/zulu.list
RUN apt-get -qq update
RUN apt-get -qqy install zulu-7=7.20.0.3
