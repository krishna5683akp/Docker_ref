FROM openjdk:11
LABEL author="krishnaprasad"
LABEL project="spc as non root user"
ARG user=krishna
ARG group=ubuntu
ARG uid=1000
ARG gid=1000
RUN groupadd -g ${gid} ${group} && \
    useradd  -u ${uid} -g ${gid} -m -s /bin/bash ${user}
USER ${user}
ADD https://referenceapplicationskhaja.s3.us-west-2.amazonaws.com/spring-petclinic-2.4.2.jar /spring-petclinic-2.4.2.jar
EXPOSE 8080
WORKDIR /spring-petclinic
CMD [ "java" , "-jar" , "spring-petclinic-2.4.2.jar " ]