# LLVMgold plugin

LLVM 8.0
 - make sure you have `makeinfo` of version 4.8. If not, go install texinfo-4.8
 - `git clone --depth 1 git://sourceware.org/git/binutils-gdb.git binutils`
 - `cd binutils && mkdir build && cd build`
 - `../configure --enable-gold --enable-plugins --disable-werror`
 - `make all-gold`
 - [official guide](https://bcain-llvm.readthedocs.io/projects/llvm/en/latest/GoldPlugin/)
