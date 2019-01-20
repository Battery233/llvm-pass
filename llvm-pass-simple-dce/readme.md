# llvm-pass-simple-dce

You will use Git to clone the LLVM sources and Cmake to generate the Makefiles to build LLVM on Linux. A minimum of Cmake 3.4 or later is required.

To run the pass:

$ clang -S -emit-llvm -Xclang -disable-O0-optnone test.c

$ opt -load skeleton/libSkeletonPass.so -mem2reg -skeletonpass test.ll -o new.ll -S