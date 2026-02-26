Here you will find:
-README.md (this file you are reading at the momment)
-innoextract-1.9-zd.patch for patching official release innoextract-1.9.tar.gz from https://github.com/dscharrer/innoextract/releases
-innoextract-1.10-zd.patch this can patch current 2026.02 git from https://github.com/dscharrer/innoextract

Just a quick hack to compile official package innoextract-1.9.tar.gz on 2026 Slackware current ...

$ tar xf innoextract-1.9.tar.gz 
$ cd innoextract-1.9
$ cat ../innoextract-1.9-zd.patch |patch -p1
patching file CMakeLists.txt
patching file cmake/VersionScript.cmake
patching file src/stream/slice.cpp
$ mkdir build && cd build
$ cmake ../
$ make -j8
