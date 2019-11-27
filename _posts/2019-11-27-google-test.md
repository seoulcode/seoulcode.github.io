---
layout: post
title:  "[testing] how use googletest "
date:   2019-11-27. (수) 15:43:23 KST
categories: [testing, googletest]
---


1. 샘플로 사용할 디렉토리로 이동. 
`$> cd gtest-sample`

1. I use it as a library in my project, so I clone the googletest source in the project's subdirectory. 프로젝트에서 라이브러리로 사용하므로 프로젝트의 하위 디렉토리에 구글 테스트 소스를 클론 받는다. 
`$> g clone https://github.com/google/googletest.git gtest`

1. googletest를 빌드
`$> cd googletest/googletest/`
1. cmake를 빌드할 디렉토리 생성, cmake 실행.
```bash
$> mkdir build
$> cd build
$> cmake ..
```
	- if the following error occur, `No CMAKE_CXX_COMPILER could be found.`, install the g++ `$> sudo apt-get install g++`
1. retry cmake build.
```bash
c192~/work/gtest-sample/googletest/googletest/build> cmake ..
-- The CXX compiler identification is GNU 7.4.0
-- The C compiler identification is GNU 7.4.0
-- Check for working CXX compiler: /usr/bin/c++
-- Check for working CXX compiler: /usr/bin/c++ -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Check for working C compiler: /usr/bin/cc
-- Check for working C compiler: /usr/bin/cc -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Detecting C compile features
-- Detecting C compile features - done
-- Found PythonInterp: /usr/bin/python (found version "2.7.15") 
-- Looking for pthread.h
-- Looking for pthread.h - found
-- Looking for pthread_create
-- Looking for pthread_create - not found
-- Looking for pthread_create in pthreads
-- Looking for pthread_create in pthreads - not found
-- Looking for pthread_create in pthread
-- Looking for pthread_create in pthread - found
-- Found Threads: TRUE  
-- Configuring done
-- Generating done
-- Build files have been written to: ~/work/gtest-sample/googletest/googletest/build
c192~/work/gtest-sample/googletest/googletest/build>
```

1. run make
```bash
c192~/work/gtest-sample/googletest/googletest/build> make
Scanning dependencies of target gtest
[ 25%] Building CXX object CMakeFiles/gtest.dir/src/gtest-all.cc.o
[ 50%] Linking CXX static library lib/libgtest.a
[ 50%] Built target gtest
Scanning dependencies of target gtest_main
[ 75%] Building CXX object CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
[100%] Linking CXX static library lib/libgtest_main.a
[100%] Built target gtest_main
c192~/work/gtest-sample/googletest/googletest/build>
```


