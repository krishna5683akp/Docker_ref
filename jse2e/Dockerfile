FROM ubuntu:22.04 
LABEL PROJECT="jse2e"
LABEL owner="krishnaprasad"
RUN git clone https://github.com/krishna5683akp/js-e2e-express-server.git && \
    cd js-e2e-express-server && \
    apt-get install nodejs -y && \
    apt-get install npm -y
EXPOSE 3000
CMD [ "npm","start" ]

