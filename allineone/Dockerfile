FROM registry.cn-shanghai.aliyuncs.com/bcx86/itop:base

RUN apt-get update && apt-get install -y mariadb-server pwgen \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* \
    && rm -rf /var/lib/mysql/*
    # Remove pre-installed database

COPY service /etc/service/
COPY artifacts/scripts /
COPY run.sh /run.sh
RUN chmod +x -R /etc/service \
    && chmod +x /*.sh

VOLUME /var/lib/mysql

EXPOSE 3306
