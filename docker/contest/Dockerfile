FROM golang:1.15.4-buster

RUN apt-get update && apt-get install -y mariadb-client

RUN go get -t -v ./...
WORKDIR ${GOPATH}/src/github.com/facebookincubator/contest
COPY  . .
RUN go get -t -v ./...
RUN chmod a+x docker/contest/tests.sh
