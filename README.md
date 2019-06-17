This fork of sgminer-gm supports mining LBRY in both Stratum pools and directly to a local LBRYcrd instance.

#### Example:
```
# compile the thing:
git clone https://github.com/lbryio/sgminer-gm
cd sgminer-gm
git submodule init
git submodule update
./autogen.sh  # has to run after submodule stuff
./configure CFLAGS="-O3 -march=native -I/usr/lib/cuda-10.1/targets/x86_64-linux/include -L/usr/lib/cuda-10.1/targets/x86_64-linux/lib"
make -j10

# start mining on testnet:
./sgminer -k lbry -O ruser:rpswd -o "http://127.0.0.1:19245" 
```

Substitute the cuda paths for your local OpenCL installation location. Please refer to the documentation found upstream for further build instructions, etc. 