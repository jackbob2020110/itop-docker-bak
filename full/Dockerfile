FROM registry.cn-shanghai.aliyuncs.com/bcx86/itop:v3.0
MAINTAINER Jun

RUN apt install -y mariadb-server

COPY service /etc/service/
COPY artifacts/scripts /
COPY run.sh /run.sh
RUN chmod +x -R /etc/service \
    && chmod +x /*.sh

VOLUME /var/lib/mysql

EXPOSE 3306
