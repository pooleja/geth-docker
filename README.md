# Geth Docker

This repo is adopted from [Kunstmaan/docker-ethereum](https://github.com/Kunstmaan/docker-ethereum).

The main changes are:
* Turn off mining on the testnet node
* Add a volume on the base image so that accounts/chain data is not lost.

### Running a Testnet Node
```
$ docker pull pooleja/geth-testnet
$ docker run pooleja/geth-testnet
```

### Attaching to Node
You can attach to the bash shell of the node to get on the geth console:
```
$ docker exec -i -t <CONTAINER_ID> /bin/bash
# geth attach ipc:/root/.ethereum/testnet/geth.ipc
```
From the geth console you can check if it is finished syncing:
```
> eth.syncing
false
```
If it is still syncing you will see stats about the sync instead of `false`.