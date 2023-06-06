FROM ubuntu:22.04 as build
RUN apt update && \
    apt install openjdk-8-jdk -y && \
    apt install maven -y && \
    apt install git -y &&  \
    git clone https://github.com/wakaleo/game-of-life.git && cd game-of-life && \
    mvn package
FROM tomcat:9.0-jdk8-corretto
WORKDIR /root/
COPY --from=build /game-of-life/gameoflife-web/target/gameoflife.war /usr/local/tomcat/webapps/gameoflife.war
EXPOSE 9090
CMD ["catalina.sh", "run"] 