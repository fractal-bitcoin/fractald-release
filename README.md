# Fractal Bitcoin Overview

**Website:** [Fractal Bitcoin](https://fractalbitcoin.io)

## What is Fractal Bitcoin?

Fractal Bitcoin is the only Bitcoin scaling solution that uses the Bitcoin Core code itself to recursively scale unlimited layers on top of the world’s most-secure and -held blockchain.

It is the first instance of a virtualization methodology applied to Bitcoin in the world. Fractal gradually extends the Bitcoin blockchain into a scalable computing system without breaking consistency with the Bitcoin main chain.

With strong tooling and support, building on Fractal is straightforward.

## Build Fractal Bitcoin

The following are developer notes on how to build Bitcoin Core on your native platform. They are not complete guides, but include notes on the necessary libraries, compile flags, etc.

- [Dependencies](https://github.com/fractal-bitcoin/fractal/blob/main/doc/dependencies.md)
- [macOS Build Notes](https://github.com/fractal-bitcoin/fractal/blob/main/doc/build-osx.md)
- [Unix Build Notes](https://github.com/fractal-bitcoin/fractal/blob/main/doc/build-unix.md)
- [Windows Build Notes](https://github.com/fractal-bitcoin/fractal/blob/main/doc/build-windows.md)
- [FreeBSD Build Notes](https://github.com/fractal-bitcoin/fractal/blob/main/doc/build-freebsd.md)
- [OpenBSD Build Notes](https://github.com/fractal-bitcoin/fractal/blob/main/doc/build-openbsd.md)
- [NetBSD Build Notes](https://github.com/fractal-bitcoin/fractal/blob/main/doc/build-netbsd.md)
- [Android Build Notes](https://github.com/fractal-bitcoin/fractal/blob/main/doc/build-android.md)

## Running Fractal Bitcoin

**Run on linux:**

1. Download the release:

```bash
wget https://github.com/fractal-bitcoin/fractald-release/releases/download/v0.2.2/fractald-0.2.2-x86_64-linux-gnu.tar.gz
```

2. Extract the files:

```bash
tar -zxvf fractald-0.2.2-x86_64-linux-gnu.tar.gz
```

3. Navigate to the directory:

```bash
cd fractald-0.2.2-x86_64-linux-gnu
```

4. Set up the data directory:

```bash
mkdir data
```

5. Run the Bitcoin daemon:

```bash
./bin/bitcoind -datadir=./data/
```

**Using Docker:**

1. Clone the repository:

```bash
git clone https://github.com/fractal-bitcoin/fractald-release.git
```

2. Navigate to the Docker directory:

```bash
cd fractald-docker
```

3. Start the service with Docker Compose:

```bash
docker-compose up -d
```

## Configuration

### Runing Fractal Bitcoin Testnet

Edit `bitcoin.conf` to add the following parameters.

```
testnet=1

[testnet]
```

## Recommended configuration

### For full node

- 2 cores CPU
- 8 GB memory
- Disk space:
  - Mainnet: 800 GB
  - Testnet: 300 GB

### For mining node

- 2 cores CPU
- 4 GB memory
- 50 GB disk space.

Edit `bitcoin.conf` to add the following parameters.

```
prune=50000
```
