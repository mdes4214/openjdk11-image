FROM adoptopenjdk/openjdk11:x86_64-debian-jdk-11.0.13_8
# FROM adoptopenjdk/openjdk11:x86_64-debianslim-jdk-11.0.13_8

COPY ./mariadb-10.6.5-linux-systemd-x86_64.tar.gz mariadb.tar.gz

RUN tar -zxvf mariadb.tar.gz && rm mariadb.tar.gz
RUN mv mariadb-* /home/mariadb
RUN groupadd mysql
RUN useradd -g mysql mysql
RUN cd /usr/local
RUN ln -s /home/mariadb mysql
RUN cd mysql
# RUN ./scripts/mysql_install_db --user=mysql

# # RUN chown -R mysql .
# # RUN chgrp -R mysql .
# RUN chown -R root .
# RUN chown -R mysql data

# RUN chmod -R 777 .

# RUN cp support-files/mysql.server /etc/init.d/mysqld