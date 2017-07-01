NetsCoin
========

![NetsCoin Logo](https://avatars3.githubusercontent.com/u/29796172?v=3&s=460)

Technical Parameters
--------------------

Coin Abbreviation (Ticker): NTC

Consensus Type: PoW

Hashing Algorithm: Scrypt

Difficulty Retargeting: Kimoto Gravity Well

Time Between Blocks: 60 seconds

Initial Block Reward: 10,000

Halving every 2,000,000 blocks

Total Coins: 50,000,000,000

Connections
-----------

Node IPs:

67.205.183.188

rpc port: 24298
net port: 24299

How To Compile
--------------

```
apt-get update && apt-get upgrade
apt-get install ntp git build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev libqrencode-dev

wget http://miniupnp.free.fr/files/download.php?file=miniupnpc-1.8.tar.gz && tar -zxf download.php\?file\=miniupnpc-1.8.tar.gz && cd miniupnpc-1.8/
make && make install && cd .. && rm -rf miniupnpc-1.8 download.php\?file\=miniupnpc-1.8.tar.gz

git clone https://github.com/netscoin/netscoin

cd netscoin/src
make -f makefile.unix USE_UPNP=1 USE_QRCODE=1 USE_IPV6=1
strip NetsCoin
```

How To Mine
-----------

You can use tools like `cgminer` or mine directly using the compiled wallet by writing into your ~/.NetsCoin/NetsCoin.conf:

```
gen=1
```
