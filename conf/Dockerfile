FROM amazonlinux:latest

RUN yum update -y
RUN yum install yum-utils -y


RUN yum-config-manager --add-repo=https://jdl-circleci.s3.amazonaws.com/clamav/pub/repos/clamav.repo
RUN yum makecache

CMD echo yum --disablerepo=* --enablerepo=clamav info clamav-update | grep Version | awk -F':' '{ print $2 }' | tail -n1 | tr -d '[:space:]'