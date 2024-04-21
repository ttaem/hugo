---
title: "라즈베리파이에 eBPF 환경 설정"
date: 2024-04-20T20:14:06+09:00
draft: false
---

## 커널 설정
기본으로 설정되어 있다. 나중에 추가 예정

## 패키지 설치

{{< highlight bash  >}}
root@cklee5:/home/pi# apt-get install bpfcc-tools
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following additional packages will be installed:
  ieee-data libbpfcc python-bpfcc python-netaddr
  Suggested packages:
    ipython python-netaddr-docs
    The following NEW packages will be installed:
      bpfcc-tools ieee-data libbpfcc python-bpfcc python-netaddr
      0 upgraded, 5 newly installed, 0 to remove and 158 not upgraded.
      Need to get 11.3 MB of archives.
      After this operation, 43.5 MB of additional disk space will be used.
      Do you want to continue? [Y/n] 
      Get:1 http://ftp.kaist.ac.kr/raspbian/raspbian buster/main armhf libbpfcc armhf 0.3.0-4 [8,911 kB]
      Get:2 http://ftp.kaist.ac.kr/raspbian/raspbian buster/main armhf python-bpfcc all 0.3.0-4 [22.1 kB]
      Get:3 http://ftp.kaist.ac.kr/raspbian/raspbian buster/main armhf ieee-data all 20180805.1 [1,590 kB]
      Get:4 http://ftp.kaist.ac.kr/raspbian/raspbian buster/main armhf python-netaddr all 0.7.19-1 [229 kB]
      Get:5 http://ftp.kaist.ac.kr/raspbian/raspbian buster/main armhf bpfcc-tools all 0.3.0-4 [582 kB]
      Fetched 11.3 MB in 4s (3,004 kB/s)
      Selecting previously unselected package libbpfcc.
      (Reading database ... 224059 files and directories currently installed.)
      Preparing to unpack .../libbpfcc_0.3.0-4_armhf.deb ...
      Unpacking libbpfcc (0.3.0-4) ...
      Selecting previously unselected package python-bpfcc.
      Preparing to unpack .../python-bpfcc_0.3.0-4_all.deb ...
      Unpacking python-bpfcc (0.3.0-4) ...
      Selecting previously unselected package ieee-data.
      Preparing to unpack .../ieee-data_20180805.1_all.deb ...
      Unpacking ieee-data (20180805.1) ...
      Selecting previously unselected package python-netaddr.
      Preparing to unpack .../python-netaddr_0.7.19-1_all.deb ...
      Unpacking python-netaddr (0.7.19-1) ...
      Selecting previously unselected package bpfcc-tools.
      Preparing to unpack .../bpfcc-tools_0.3.0-4_all.deb ...
      Unpacking bpfcc-tools (0.3.0-4) ...
      Setting up ieee-data (20180805.1) ...
      Setting up python-netaddr (0.7.19-1) ...
      Setting up libbpfcc (0.3.0-4) ...
      Setting up python-bpfcc (0.3.0-4) ...
      Setting up bpfcc-tools (0.3.0-4) ...
      Processing triggers for man-db (2.8.5-2) ...
      Processing triggers for libc-bin (2.28-10+rpi1) ...
{{< / highlight >}}

## 설치 확인

tcplife-bpfcc 를 실행해 본다.

{{< highlight bash  >}}
ceback (most recent call last):
  File "/usr/sbin/tcplife-bpfcc", line 24, in <module>
      from bcc import BPF
      ModuleNotFoundError: No module named 'bcc'`
{{< / highlight >}}

에러가 발생한다.  
확인해 보니 python2에 설치가 되어있다.

{{< highlight bash  >}}
root@cklee5:/usr/lib/python2.7# !f
find . -name "*bcc*"
./dist-packages/jinja2/bccache.pyc
./dist-packages/jinja2/bccache.py
./dist-packages/bcc-0.3.0.egg-info
./dist-packages/bcc
./dist-packages/bcc/libbcc.pyc
./dist-packages/bcc/libbcc.py
{{< / highlight >}}

python3로 설치하는 방법이 있다.

{{< highlight bash  >}}
root@cklee5:/home/pi# sudo apt-get install -y python3-bpfcc
{{< / highlight >}}

다시 실행해 본다. 커널 빌드 정보가 없다. 지금 내 보드는 직접 크로스 컴파일한 커널을 이미지와 모듈들만 수동으로 가져와서 추가 빌드에 필요한 부분이 필요한 것 같다.  
일단 라즈베리파이에서 직접 빌드한 커널이 있는 보드가 있어 거기에서 우선 작업한다.

{{< highlight bash >}}
pi@cklee7:~/work $ tcplife-bpfcc
python3: /usr/lib/llvm-11/include/llvm/ADT/PointerIntPair.h:178: static intptr_t llvm::PointerIntPairInfo<PointerT, IntBits, PtrTraits>::updatePointer(intptr_t, PointerT) [with PointerT = clang::Stmt*; unsigned int IntBits = 1; PtrTraits = llvm::PointerLikeTypeTraits<clang::Stmt*>; intptr_t = int]: Assertion `(PtrWord & ~PointerBitMask) == 0 && "Pointer is not sufficiently aligned"' failed.
Aborted
{{< / highlight >}}

생전 처음보는 에러가 발생한다. 구글링해도 나오질 않는다. 큰일이다.


```bash
git commit
ls -la
```

```ruby 
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```


{{< highlight bash  >}}
{{< / highlight >}}
