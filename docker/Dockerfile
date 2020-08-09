FROM python:3.7

USER root

RUN mkdir -p /usr/src
WORKDIR /usr/src
ADD src /usr/src/
ADD requirements.txt /usr/src/
ADD credential /usr/src/credential/

RUN apt-get update
RUN apt-get -y install jq
RUN apt-get -y install locales && \
    localedef -f UTF-8 -i ja_JP ja_JP.UTF-8
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
ENV TZ JST-9
ENV TERM xterm

RUN apt-get install -y vim less
RUN pip install --upgrade pip
RUN pip install --upgrade setuptools
RUN pip install -r requirements.txt
RUN aws configure set aws_access_key_id `jq -r '.AccessKeyId' ./credential/aws_credentials.json`
RUN aws configure set aws_secret_access_key `jq -r '.SecretAccessKey' ./credential/aws_credentials.json`
RUN aws configure set region ap-northeast-1
