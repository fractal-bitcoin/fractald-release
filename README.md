# Fractal Bitcoin

https://fractalbitcoin.io

## What is Fractal Bitcoin

Fractal Bitcoin is the only Bitcoin scaling solution that uses the Bitcoin Core code itself to recursively scale unlimited layers on top of the world’s most secure and most held blockchain.

It is the first instance of a virtualization methodology applied to Bitcoin in the world. Fractal Bitcoin gradually extends the Bitcoin blockchain into a scalable computing system without breaking consistency with the Bitcoin main chain.

With strong tooling and support, building on Fractal is straightforward.

## Run

### Run on Linux

This requires `git` to be installed on the system.

```
git clone https://github.com/fractal-bitcoin/fractald-release.git

cd fractald-release
cd fractald-x86_64-linux-gnu

mkdir data
cp ./bitcoin.conf ./data
./bin/bitcoind -datadir=./data/ -maxtipage=504576000

```

### Run with Docker on Linux

This requires `git` and Docker to be installed on the system.\
For details on how to install docker, visit the official documentation here: https://docs.docker.com/desktop/install/linux-install/

```
git clone https://github.com/fractal-bitcoin/fractald-release.git

cd fractald-release
cd fractald-docker

docker-compose up -d
```
