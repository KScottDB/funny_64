# Funny 64

- This repo contains edits to the SM64 Decompilation codebase to make it Funny

Funny 64 can be built with similarities to the JP and EU copies of SM64, but I don't recommend this.
Please build it as US. (`make VERSION=us`)

I didn't modify the ability for assets to be imported from the JP or EU versions, so go right ahead and use those as `baserom.**.z64` if it's easier for you.

Otherwise, the instructions to build Funny 64 are exactly the same as the SM64 decomp.

# Build instructions (Ubuntu/Debian)

Install build dependencies:
```
sudo apt install -y build-essential git binutils-mips-linux-gnu python3 libaudiofile-dev
```

Download latest package from [qemu-irix Releases](https://github.com/n64decomp/qemu-irix/releases) and install:
```
wget https://github.com/n64decomp/qemu-irix/releases/download/v2.11-deb/qemu-irix-2.11.0-2169-g32ab296eef_amd64.deb
sudo dpkg -i qemu-irix-2.11.0-2169-g32ab296eef_amd64.deb
rm qemu-irix-2.11.0-2169-g32ab296eef_amd64.deb
```

Download this repo and build:
```
git clone https://github.com/KScottDB/funny_64.git
cd funny_64
make VERSION=US -j16
```

(the `-j` parameter should be equal to the amount of cores you have for fastest build.

e.g. `-j2` on a dual core, `-j4` on a quad core, etc...)
