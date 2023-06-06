FROM ubuntu:22.04
LABEL project="sprin-petclinic"
LABEL author="krishnaprasad"
ARG user=krishna
ARG group=ubuntu
ARG uid=1000
ARG gid=1000
RUN groupadd -g ${gid} ${group} && \
    useradd  -u ${uid} -g ${gid} -m -s /bin/bash ${user} && \
    #echo $user ALL=\(root\) NOPASSWD:ALL > /etc/sudeors.d/$user && \
    #chmod 0440 /etc/sudeors.d/$user
RUN apt update && \
    apt install openjdk-11-jdk -y && \
    apt install wget -y && \ 
    apt install sudo -y && \
    wget https://referenceapplicationskhaja.s3.us-west-2.amazonaws.com/spring-petclinic-2.4.2.jar
USER ${user}
EXPOSE 8080
CMD [ "java" , "-jar" , "spring-petclinic-2.4.2.jar" ]