# FROM almalinux:9
# RUN printf '%s\n' \
#     '[mongodb-org-7.0]' \
#     'name=MongoDB Repository' \
#     'baseurl=https://repo.mongodb.org/yum/redhat/9/mongodb-org/7.0/x86_64/' \
#     'enabled=1' \
#     'gpgcheck=0' \
#     > /etc/yum.repos.d/mongo.repo
    
# RUN dnf install -y mongodb-org
# RUN sed -i 's/127\.0\.0\.1/0.0.0.0/g' /etc/mongod.conf
# EXPOSE 27017
# CMD ["mangod", "-g", "daemonoff"]
FROM almalinux:9

RUN printf '%s\n' \
    '[mongodb-org-7.0]' \
    'name=MongoDB Repository' \
    'baseurl=https://repo.mongodb.org/yum/redhat/9/mongodb-org/7.0/x86_64/' \
    'enabled=1' \
    'gpgcheck=0' \
    > /etc/yum.repos.d/mongo.repo

RUN dnf install -y mongodb-org

RUN sed -i 's/127\.0\.0\.1/0.0.0.0/g' /etc/mongod.conf

EXPOSE 27017

CMD ["mongod", "--config", "/etc/mongod.conf"]