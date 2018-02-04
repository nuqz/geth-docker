### Clone

```
$ git clone git@github.com:nuqz/geth-docker.git
$ cd geth-docker
```

### Build

```
$ docker build ./geth -t geth-build-env
$ docker build ./solidity -t solidity-build-env
```

### Init private network

Note, you should configure `config/genesis.json` manually and put `networkid` and `etherbase` values into the `docker-compose.yml`.

```
$ docker-compose run miner ./bin/geth --datadir ./data init ./config/genesis.json
```

### Run

```
$ docker-compose up -d miner
```

### Console

```
$ docker-compose exec miner ./bin/geth attach ./data/geth.ipc
```

### Advanced

At the build stage you can use [geth-micro](https://github.com/nuqz/go-ethereum) version of node to reduce miner's memory & disk usage. This option is suitable for devices like RaspberryPi, BananaPi, etc.

Just swap "wget" lines in `./geth/Dockerfile`.

## Thanks
