###   --------------------------------
###                                 --
###          ss/alpine-3.8          --
###   修改自官方镜像 参考秋水逸冰脚本  --
###   --------------------------------

FROM debian:wheezy-slim

LABEL maintainer coze <zeoco1132@gmail.com>

ENV TZ "Asia/Shanghai"

ENV FILE_PATH /usr/local/bin/
# RUN mkdir -p ${FILE_PATH}

ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install --assume-yes apt-utils

COPY ./ss-go-* ${FILE_PATH}

RUN set -xe && \
    cd ${FILE_PATH} && \
    ss-go-install

RUN rm -rf /var/lib/apt/lists/*