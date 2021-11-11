FROM adoptopenjdk/openjdk11:x86_64-debian-jdk-11.0.13_8
# FROM adoptopenjdk/openjdk11:x86_64-debianslim-jdk-11.0.13_8

COPY ./mongodb-linux-x86_64-debian10-4.4.10.tgz mongodb.tgz
# COPY ./mongodb-linux-x86_64-debian10-5.1.0.tgz mongodb.tgz

RUN tar -zxvf mongodb.tgz && rm mongodb.tgz
RUN mv mongodb-* /etc/mongodb
RUN mkdir -p /data/db
RUN chmod -R 777 /data