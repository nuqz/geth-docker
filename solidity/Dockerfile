FROM alpine AS solidity-build-env
RUN apk update && apk upgrade && apk add git
WORKDIR /tmp
RUN git clone --recursive https://github.com/ethereum/solidity.git
WORKDIR /tmp/solidity
RUN mkdir build
WORKDIR /tmp/solidity/build
RUN ../scripts/install_deps.sh && cmake .. && make
