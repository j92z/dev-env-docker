FROM golang:1.11.5-stretch

COPY file/* /tmp/

ENV GO111MODULE auto
ENV GOPROXY https://goproxy.io

RUN rm -f /etc/apt/sources.list && mv /tmp/deb.list /etc/apt/sources.list

WORKDIR $GOPATH