# !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
# NOTE: DO *NOT* EDIT THIS FILE.  IT IS GENERATED.
# PLEASE UPDATE Dockerfile.txt INSTEAD OF THIS FILE
# !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
FROM imprev/node-firefox
MAINTAINER Selenium <selenium-developers@googlegroups.com>

USER root

#====================================
# Scripts to run Selenium Standalone
#====================================
COPY entry_point.sh /opt/bin/entry_point.sh
RUN chmod +x /opt/bin/entry_point.sh

RUN apt-get update
RUN apt-get install -y iputils-ping curl tar

curl -o http://github.com/mozilla/geckodriver/releases/download/v0.11.1/geckodriver-v0.11.1-linux32.tar.gz | tar zxf -C /usr/local/bin/geckodriver

USER seluser

EXPOSE 4444
