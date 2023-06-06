FROM jelastic/nginxphp
LABEL author="krishna"
LABEL PROJECT="moodle"
ARG user=krishna
ARG group=ubuntu
ARG uid=1000
ARG gid=1000
RUN yum install git -y && \
    cd /opt && \
    git clone git://git.moodle.org/moodle.git && \
    cd moodle && \
    git checkout MOODLE_400_STABLE && \
    cp -R /opt/moodle /var/www/html/ && \
    mkdir /var/moodledata && \
    cp -R /opt/moodle /var/www/html/ && \
    cp -R /opt/moodle /var/www/html/ && \
    chown -R www-data /var/moodledata && \
    chmod -R 777 /var/moodledata && \
    chmod -R 0755 /var/www/html/moodle 
RUN chmod -R 777 /var/www/html/moodle && \
    chmod -R 777 /var/www/html/moodle
