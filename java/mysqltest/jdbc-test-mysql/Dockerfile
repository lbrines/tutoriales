FROM registry.access.redhat.com/ubi7/ubi

RUN yum -y install java-11-openjdk-devel && yum clean all && rm -rf /var/cache/yum

WORKDIR /app
COPY ./target/jdbcTestMySql.jar .
ADD ./run.sh .

CMD ["sh","run.sh"]
