FROM maven:3.8.6-openjdk-11 as build
ARG BRANCH=main
RUN git clone https://github.com/spring-projects/spring-petclinic.git && \
    cd /spring-petclinic && \
    git checkout ${BRANCH} && \
    mvn package

### jar location /spring-petclinic/target/spring-petclinic-2.7.3.jar
FROM openjdk:11
LABEL "project" = "spc"
LABEL "author" = "krishnaprasad"
ARG user=krishna
ARG group=ubuntu
ARG uid=1000
ARG gid=1000
RUN groupadd -g ${gid} ${group} && \
    useradd  -u ${uid} -g ${gid} -m -s /bin/bash ${user}
USER ${user}
EXPOSE 8080
COPY --from=build /spring-petclinic/target/spring-petclinic-2.7.3.jar /spring-petclinic-2.7.3.jar
CMD ["java", "-jar", "spring-petclinic-2.7.3.jar"]
