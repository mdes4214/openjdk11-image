FROM adoptopenjdk/openjdk11:x86_64-debian-jdk-11.0.13_8
# FROM adoptopenjdk/openjdk11:x86_64-debianslim-jdk-11.0.13_8

COPY ./minio_20211109032145.0.0_amd64.deb minio.deb

RUN dpkg -i minio.deb  && rm minio.deb
RUN printf '#!/bin/bash\nminio server /mnt/data --console-address ":9001"' >> minio-server-default.sh
RUN chmod +x /minio-server-default.sh
RUN chmod -R 777 /mnt