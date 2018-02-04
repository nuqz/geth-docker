FROM alpine
RUN apk update && apk upgrade && mkdir /ethereum
WORKDIR /ethereum
RUN  mkdir bin
COPY --from=geth-build-env /tmp/go-ethereum/build/bin/geth ./bin/geth
COPY --from=solidity-build-env /tmp/solidity/build/solc/solc ./bin/solc
