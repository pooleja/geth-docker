# Geth Docker

This repo is adopted from [Kunstmaan/docker-ethereum](https://github.com/Kunstmaan/docker-ethereum).

The main changes are:
* Turn off mining on the testnet node
* Add a volume on the base image so that accounts/chain data is not lost.
