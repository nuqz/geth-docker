FROM golang:alpine AS geth-build-env
RUN apk update && apk upgrade && apk add wget git alpine-sdk linux-headers
WORKDIR /tmp
# RUN wget -o v1.7.3.tar.gz https://github.com/nuqz/go-ethereum/archive/micro.tar.gz
RUN wget https://github.com/ethereum/go-ethereum/archive/v1.7.3.tar.gz
RUN mkdir /tmp/go-ethereum && tar -xvf v1.7.3.tar.gz -C /tmp/go-ethereum --strip-components=1
WORKDIR /tmp/go-ethereum
RUN make geth
