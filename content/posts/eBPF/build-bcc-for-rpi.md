---
title: "Build Bcc for Rpi"
date: 2024-05-07T11:46:25+09:00
draft: true
---

# BCC 빌드
소스 다운로드 및 빌드
```
git clone https://github.com/iovisor/bcc.git
mkdir bcc/build; cd bcc/build
cmake ..
make
sudo make install
```
그러나, 우리는 RPI 에 사용할 바이너리가 나와야 한다.
## 크로스 컴파일 사전 작업
### cmake 에서 크로스 컴파일
https://amgaera.github.io/blog/2014/04/10/cross-compiling-for-raspberry-pi-on-64-bit-linux/   를 참조하여 만든다.

# LLVM 빌드


