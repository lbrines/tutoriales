FROM registry.access.redhat.com/ubi7/ubi
#FROM registry.access.redhat.com/ubi8/openjdk-11:1.3
USER root
RUN useradd apisearch

RUN yum -y install java-11-openjdk-devel && yum clean all && rm -rf /var/cache/yum

WORKDIR /app
COPY ./target/jdbcTestMySql.jar .
ADD ./run.sh .

CMD ["sh","run.sh"]
