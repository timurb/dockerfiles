###
### Base image starts here
###
FROM ubuntu
MAINTAINER Timur Batyrshin <erthad@gmail.com>

RUN apt-get update
RUN apt-get -y dist-upgrade
RUN apt-get -y install curl wget git vim
###
### Do not modify anything above this line unless you want to include that in all images
###

# Install Java
RUN apt-get -y install default-jre-headless

# Install ElasticSearch 0.90.5
RUN wget http://download.elasticsearch.org/elasticsearch/elasticsearch/elasticsearch-0.90.5.deb
RUN dpkg -i elasticsearch-0.90.5.deb
RUN apt-get install -fy
RUN rm -f elasticsearch-0.90.5.deb

# Install anthracite
RUN git clone --recursive https://github.com/Dieterbe/anthracite.git /opt/anthracite
