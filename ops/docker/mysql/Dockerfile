FROM mysql:5.7.25

LABEL maintainer="eden.reich@gmail.com"

COPY config/my.cnf /etc/mysql/conf.d/my.cnf

WORKDIR /etc/mysql

CMD ["mysqld"]

EXPOSE 3306