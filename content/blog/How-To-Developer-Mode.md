+++
author = "ttaem"
categories = ["HowTo"]
date = "2018-10-01"
description = "크롬북에서 개발자 모드 활성화/비활성화 방법"
featured = ""
featuredalt = ""
featuredpath = "date"
linktitle = ""
title = "크롬북에서 개발자 모드 활성화/비활성화 방법"
type = "post"

+++

## 시작 

시장에서 Chromebook 과 Chrome OS 가 주목받는 이유는 그것의 단순함 때문이다. 또한, 최근에 Android App 과 Native Linux 를 지원함에 따라 점점 강력해지고 있다. 또한, Chrome OS 는 강력한 보안 기능을 가지고 있어 라이트 PC 유저들이 사용하기에 적합하다.

이러한 특징들은 도리어 개발자들이 접근하기에는 어려운 부분이 있는데, 다행스럽게도 Chrome OS 는 **개발자 모드** 를 활성화할 수 있는 방법을 제공한다. 이것은 마치 Android Device 에서 root 권한을 얻는 것과 같다.

이 글은 개발자 모드를 활성화 하는 방법에 대하여 살펴보도록 하겠다.

## Chromebook 에서 개발자 모드 활성화 하기

1. 가장 먼저 chromebook 에 저장된 중요한 데이타를 백업한다. 개발자 모드를 활성화하게 되면 로그인 정보와 모든 저장된 정보가 날아간다. 이 정보들은 어떠한 경우라도 복구가 불가능하다. 
2. Chromebook 이 켜져 있으면 끈다.
3. 모드를 변경하기 위해서는 반드시 복구 모드(recovery mode) 로 먼저 들어가야 한다. 복구 모드로 들어가는 방법은 다음과 같다. 이미 커버는 열려진 상태일 것이고, 이 상태에서 ESC 키와 Refresh 키(ESC 키 오른쪽 3번째, 동근 모양의 화살표키) 를 누른 상태에서 전원 키를 누른다.
4. 다음 메세지가 나올 때까지 계속 누르고 있는다. (영어는 “Chrome OS is missing or damaged. Please insert USB stick.”, 한글은 "Chrome OS가 없거나 손상되었습니다. 복구 USB 메모리 또는 SD 카드를 삽입하세요") 공포스럽게 느껴지겠지만 별거 아니니 다음 절차를 따라간다.
5. Ctrl 키를 누른 상태에서 D 키를 누른다. (Ctrl + D) 
6. 만약 추가로 필요하다면, Enter 키를 누른다.
7. 재부팅 할 때까지 기다리고, 구입 후 처음 하였던 설정 과정을 하면 된다.

## Chromebook 에서 개발자 모드 비활성화 하기

1. 개발자 모드 활성화 하기보다 훨씬 쉽다.
2. 활성화 과정과 마찬가지로 백업은 필수이다.
3. 켜져 있으면 마찬가지로 끈다.
4. 전원 키를 누르고,  “OS verification is off” 메세지가 나타날 때, 스페이스 키를 누른다.
5. 초기 셋업 과정을 다시 진행한다.

## 개발자 모드의 제약 사항

Chromebook 에서 개발자 모드를 활성화 하는 것은 여러가지 잇점이 있다. Shell 을 실행할 수 있거나, Linux desktop 을 설치할 수도 있다. 물론 Chrome OS 개발자라면 더 할 나위 없겠다. There are a lot of advantages to enabling Developer Mode on your Chromebook. It gives you access to the developer shell, allows you to install a standard Linux desktop environment, and is something you will need to enable if you are a Chrome OS developer. Developer Mode is certainly not for the average user and some amount of technical know-how is needed to take full advantage of this mode.

However, there are a few disadvantages that you need to be wary of as well.

Google doesn’t support Developer Mode, so you may be at risk of voiding your device warranty.
All the security features are disabled when Developer Mode is turned on.
You lose your data when enabling or disabling Developer Mode. As you can see from the steps required to disable it, an accidental press of the space bar at the wrong time is all you need to lose all your data once again. Making continuous backups if you’re working on something important is definitely recommended.
Chromebooks boot up extremely fast. But that is a feature you will lose when Developer Mode is enabled.
