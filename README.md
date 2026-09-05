A transaction bypassing the public mempool. Private sending. Pool reward: 1.5 BTC. Modified Bitcoin-31.0 client. To receive the reward, simply build the client, add rawtx to a local pool, and find a block.

==========

===
sudo apt update && sudo apt install -y \
  build-essential libtool autotools-dev automake pkg-config bsdmainutils python3 \
  libevent-dev libboost-dev libboost-system-dev libboost-filesystem-dev \
  libboost-test-dev libsqlite3-dev cmake3 cmake
  
===

git checkout v31.0
  
===
mkdir build && cd build

===
cmake .. -DBUILD_BITCOIN_QT=OFF -DENABLE_IPC=OFF

===
make -j$(nproc)

===
cd bin && ./bitcoind

====
