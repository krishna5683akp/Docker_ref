FROM maven:3.8.6-openjdk-11 as build
#ARG BRANCH=master
RUN git clone https://github.com/krishna5683akp/shopizer.git && \
    cd shopizer && \
    mvn clean install 
#
FROM maven:3.8.6-openjdk-11
LABEL project = "shopizer"
LABEL author = "krishna"
EXPOSE 8080
COPY --from=build /shopizer/sm-shop/target/shopizer-sources.jar /shopizer
WORKDIR  /sm-shop
CMD ["mvn", "spring-boot:run"]




