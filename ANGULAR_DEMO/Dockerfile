FROM node:16
LABEL project ="learning"
LABEL author="krishna"
RUN git clone https://github.com/gothinkster/angular-realworld-example-app.git
RUN cd angular-realworld-example-app && npm install -g @angular/cli && npm install  
WORKDIR  /angular-realworld-example-app 
EXPOSE 4200/tcp
CMD ["ng", "serve", "--host", "0.0.0.0"]
