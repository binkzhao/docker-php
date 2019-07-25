FROM mongo:latest

MAINTAINER Bink Zhao <781270119@qq.com>

#COPY mongo.conf /usr/local/etc/mongo/mongo.conf

VOLUME /data/db /data/configdb

CMD ["mongod", "--config", "/usr/local/etc/mongo/mongo.conf"]

EXPOSE 27017