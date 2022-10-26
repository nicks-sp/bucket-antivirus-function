# This is for running preparing and running the docker image used to get the latest version from the custom repo
FROM amazonlinux:latest

RUN yum update -y
RUN yum install yum-utils -y


RUN yum-config-manager --add-repo=https://jdl-circleci.s3.amazonaws.com/clamav/pub/repos/clamav.repo
RUN yum makecache
