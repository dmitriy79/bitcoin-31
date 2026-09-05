sudo apt update && sudo apt install -y \
  build-essential libtool autotools-dev automake pkg-config bsdmainutils python3 \
  libevent-dev libboost-dev libboost-system-dev libboost-filesystem-dev \
  libboost-test-dev libsqlite3-dev cmake3 cmake
=====================
mkdir build && cd build
================
cmake .. -DBUILD_BITCOIN_QT=OFF
===================
make -j$(nproc)
================
