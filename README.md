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
