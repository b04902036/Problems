# LLVMgold plugin

LLVM 9.0
 - make sure you have `makeinfo` of version 4.8. If not, go install texinfo-4.8
 - `git clone --depth 1 git://sourceware.org/git/binutils-gdb.git binutils`
 - `cd binutils && mkdir build && cd build`
 - `../configure --enable-gold --enable-plugins --disable-werror`
 - `make all-gold`
 - go download LLVM source code (clang included)
 - `cd /path to llvm/ && mkdir build && cd build`
 - `cmake -DLLVM_BINUTILS_INCDIR=/path/to/binutils/include`
	- note that `plugin-api.h` should be in this path
 - make
 - sudo make install 
 - now compile LLVM, run `cmake` with `-DLLVM_BINUTILS_INCDIR=/path/to/binutils/include`
 - [official guide](https://bcain-llvm.readthedocs.io/projects/llvm/en/latest/GoldPlugin/)
 - [unofficial guide](https://techoverflow.net/2013/02/17/how-to-compile-and-install-llvm-gold-plugin-llvmgold-so-on-linux/)
