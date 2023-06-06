FROM python:3-alpine3.10
LABEL project="hello-world"
LABEL author="krishna"
RUN mkdir /flask-hello-world
ADD   https://github.com/Sysnove/flask-hello-world.git  /flask-hello-world && \
RUN cd /flask-hello-world && \
    pip3 install flask
EXPOSE 5000
WORKDIR /flask-hello-world
CMD ["flask", "run", "-h", "0.0.0.0/0"] 
