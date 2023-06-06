FROM python:bullseye
LABEL project="hello-world"
LABEL author="krishna"
RUN git clone https://github.com/Sysnove/flask-hello-world.git /flask-hello-world && \
 cd /flask-hello-world && \
    mv hello.py app.py && \
    pip3 install flask 
EXPOSE 5000
WORKDIR /flask-hello-world
CMD ["flask", "run", "-h", "0.0.0.0/0"] 
