FROM postgres:latest

# http://stackoverflow.com/questions/32304631/docker-debian-apt-error-reading-from-server
# RUN sed -i "s/httpredir.debian.org/`curl -s -D - http://httpredir.debian.org/demo/debian/ | awk '/^Link:/ { print $2 }' | sed -e 's@<http://\(.*\)/debian/>;@\1@g'`/" /etc/apt/sources.list \
RUN sed -i "s/httpredir.debian.org/debian-mirror.sakura.ne.jp/" /etc/apt/sources.list \
      && apt-get clean \
      && apt-get update --fix-missing \
      && apt-get install -y --fix-missing postgresql-9.5-postgis-2.2
#CMD ["node", "."]
