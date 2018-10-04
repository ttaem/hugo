+++
author = "ttaem"
categories = ["Info"]
date = "2018-10-03"
description = "크롬북에서의 리눅스 구동"
featured = ""
featuredalt = ""
featuredpath = "date"
linktitle = ""
title = "크롬북에서 리눅스 구동"
type = "post"

+++


구글은 최근에 Chrome OS 에 놀랄만한 작업을 하였다. Chrome OS 상에서 Android App 을 구동할 수 있게 한 것이다. 이것은 사람들이 사용하는 스마트 폰이나 태블릿 상에서 안드로이드 앱을 깔아 실행시키듯이 동일하게 크롬북에서도 동일하게 할 수 있다는 의미이다.
이로 인해 크롬북은 더욱 강력해졌다. 그렇지만, 일부 사람들은 이것만으로 충분하다고 생각하지 않았다. 물론 보통 사람들에게는 안드로이드 앱이 구동되는 것만으로도 충분히 크롬북을 선택할 장점이 되었지만, 보다 강력한 데스크탑의 어플리케이션을 설치하고 사용하기를 원하는 사람들이 있었다. 이런 요구로 인해 리눅스가 크롬북에 등장하게 된 것이다. 
현재는 일부 크롬북에 대하여 리눅스 베타 버젼을 사용할 수 있는 기능을 제공하고 있다. (2018/10/3)

* Asus Chromebook Flip C101PA
* Acer Chromebook 11 (C732, C732T, C732L & C732LT)
* Google Pixelbook
* Samsung Chromebook Plus
* Samsung Chromebook Plus (V2)
* Lenovo Thinkpad 11e Chromebook / Lenovo Thinkpad Yoga 11e Chromebook
* Acer Chromebook Spin 11 R751T
* Acer Chromebook 15 CB515-1HT/1H
* HP Chromebook x360 11 G1 EE
* HP Chromebook x2

지원 가능한 크롬북은 안드로이드 앱을 지원하는 크롬북이 늘어났던 것처럼 점점 많아질 것으로 보인다.
이 글을 읽는 당신에게는 굉장해 보일 수 있지만, 대부분의 사람들에게는 리눅스 콘솔이 무서워 보일 수 있다. 안드로이드 앱 구동처럼 그나마 쉽게 접근하기 위해서는 다음과 같은 방법이 그나마 괜찮을 것이다.

### 리눅스 설치
먼저 리눅스 기능을 활성화 한다. 설정에 가서 Linux(Beta) 가 나올 때까지 스크롤한다. 만약 보이지 않는다면, 크롬OS가 업데이트 되었는지 확인을 한다. 그래도 없다면 아직 당신의 크롬북이 지원하지 않는 것이다.
![image](https://user-images.githubusercontent.com/1691758/46415317-fcafcb80-c75f-11e8-8eef-c1c3f8a0bf93.png)

Turn on 을 누르면 다음과 같은 창이 나타날 것이고, 인스톨을 누르면 설치를 시작한다.
![image](https://user-images.githubusercontent.com/1691758/46415384-210ba800-c760-11e8-88f4-f7d8268ae9bf.png)

인스톨이 완료되면 다음과 같은 리눅스 터미널 창이 뜨게 된다.
![image](https://user-images.githubusercontent.com/1691758/46415437-426c9400-c760-11e8-96d1-17d1d0f36828.png)

자 여기서부터 겁먹지 말고 잘 쫓아오기를 바란다.
먼저,  

> sudo apt-get update

입력한다. 다음으로 Y 를 입력하여 업데이트를 시작한다. 이 절차가 끝나면 최신 리눅스 상태가 된다.
![image](https://user-images.githubusercontent.com/1691758/46415641-a727ee80-c760-11e8-8c75-59980306e2fd.png)
다음으로,
				
> sudo apt-get install gnome-software gnome-packagekit 

을 입력한다. 마찬가지로 Y 를 입력하여 인스톨을 시작한다. 이것은 Gnome-Software-Center 를 설치하는 것으로 필요한 소프트웨어를 손 쉽게 설치할 수 있게 한다.
만약 잘 되지 않는다면 다음 절차로 하나씩 설치할 수 있다.

> sudo apt-get install <Package 이름> (ex, gimp)

### 마치며
크롬북은 점점 그 가능성을 넓혀가고 있다. 리눅스의 어플리케이션이 물론 윈도우의 그것보다 크게 좋은 점은 없다. 안드로이드 개발자에게는 크롬북에서 안드로이드 스튜디오나 이클립스로 개발을 할 수는 있을 것이지만...
어쨋거나 크롬북은 점점 더 좋은 기능들이 추가되어 가고 있으며, 앞으로 기능면에서나 사용측면에서도 분명히 더 발전할 것이다.



