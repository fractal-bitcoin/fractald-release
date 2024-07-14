# Fractal Bitcoin

https://fractalbitcoin.io

## What is Fractal Bitcoin

Fractal Bitcoin is the only Bitcoin scaling solution that uses the Bitcoin Core code itself to recursively scale unlimited layers on top of the world’s most-secure and -held blockchain.

It is the first instance of a virtualization methodology applied to Bitcoin in the world. Fractal gradually extends the Bitcoin blockchain into a scalable computing system without breaking consistency with the Bitcoin main chain.

With strong tooling and support, building on Fractal is straightforward.

## Run

### Run on linux

```
git clone https://github.com/fractal-bitcoin/fractald-release.git

cd fractald-release
cd fractald-x86_64-linux-gnu

mkdir data
cp ./bitcoin.conf ./data
./bin/bitcoind -datadir=./data/ -maxtipage=504576000

```

### Run quickly through Docker

```
git clone https://github.com/fractal-bitcoin/fractald-release.git

cd fractald-docker

docker-compose up -d
```
