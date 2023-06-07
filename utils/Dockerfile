FROM registry.access.redhat.com/ubi8/ubi:latest

RUN yum update -y \
  && yum upgrade -y \
  && yum install wget -y \
  && wget https://fastdl.mongodb.org/tools/mongosync/mongosync-rhel80-x86_64-1.3.0.tgz \
  && tar -zxvf mongosync-rhel80-x86_64-1.3.0.tgz \
  && mv mongosync-rhel80-x86_64-1.3.0/bin/mongosync /usr/local/bin \
  && rm -rf mongosync-rhel80-x86_64-1.3.0*

CMD exec /bin/bash -c "trap : TERM INT; sleep infinity & wait"
