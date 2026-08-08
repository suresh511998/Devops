FROM almalinux:9
RUN dnf install -y mongodb-org
RUN sed -i 's/127\.0\.0\.1/0.0.0.0/g' /etc/mongod.conf
CMD ["mangod", "-g", "daemonoff"]