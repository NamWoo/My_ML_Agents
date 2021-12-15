
# boot first ubuntu

>우분투를 최초로 부팅하기

목차

1. 준비물
2. 


---


## 준비물

1. 컴퓨터
   1. 랩탑
      1. 외장 그래픽 카드
   2. 데스크탑
      1. 램 (그래픽 카드의 2배)
      2. 그래픽카드 (RTX 추천)
   3. SSD-USB
      1. [외장 SSD](http://prod.danawa.com/list/?cate=11230139)
      2. [외장 USB 3.1 M.2 NVMe](http://prod.danawa.com/list/?cate=11330150)
      ![](https://www.windowscentral.com/sites/wpcentral.com/files/styles/large_wm_brw/public/field/image/2020/08/samsung-t7-laptop-1.jpg)
      ![](https://m.media-amazon.com/images/I/71HVxRs8BkL._AC_SL1500_.jpg)
2. USB
   1. ![](https://user-images.githubusercontent.com/8021479/146180912-2cc11a92-ab58-4560-b33a-e08f8a29dceb.jpg)




## USB

### download


ubuntu 20.04 다운
* https://releases.ubuntu.com/20.04/
* 파일명: `ubuntu-20.04.3-desktop-amd64.iso`



### burn USB

Ubuntu 20.04 , USB 메모리 만들기
* [Rufus를 사용하여 ubuntu 설치용 usb 메모리를 만드는 방법](https://webnautes.tistory.com/1146)
* [balena Etcher를 사용하여 ubuntu 설치용 usb 메모리를 만드는 방법](https://www.how2shout.com/linux/how-to-install-balenaetcher-on-ubuntu-20-04-lts/)


아니면 SSD USB로 
* [How To Install Linux On An External Drive Or SSD With Disk Encryption. Plug & Play on PC & MAC!](https://www.youtube.com/watch?v=gvYM6hqTkQo)


## first boot

다 완료되면 꽂고 부팅, 그리고 바이오스로 접속

* 제조사별 bios 진입 단축키 https://tks9567.tistory.com/222



### set boot 우선순위

부팅순서를 USB로 바꾸기

![](https://image5jvqbd.fmkorea.com/files/attach/new2/20210226/3254535/3204400251/3416728490/6624981a8b5ef16b555eda6fca73bbb3.jpg)



### set UEFI

Not Legacy, Yes UEFI !

* [레거시 BIOS와 UEFI 모드의 차이점 - Windows 10 BIOS 부트 모드(BOOT MODE)](https://www.tabmode.com/windows10/ueif-bios.html#gsc.tab=0)


![](https://user-images.githubusercontent.com/8021479/146155674-b243b60e-18a8-483a-98e7-e1369e56b4f7.jpeg)





## 설치 전

### nouveau 무효화

* 참고 https://qiita.com/k_ikasumipowder/items/5e88ec45f958c35e05ed


우분투 초기 부팅 전에 `nomodeset` 설정으로 그래픽 설정을 꺼줘야 한다. 그래서 install Ubuntu 선택 전에 e 키 누르면 아래와 같이 grub 화면으로 넘어갈 수 있다.


1. 선택창에서 엔터로 진입하지 말고! 
   * 20.04에서는 맨 위가 `ubuntu`
   * 18.04에서는 아래.
   * ![](https://www.wikihow.com/images/thumb/0/09/Install-Ubuntu-Linux-Step-32.jpg/v4-728px-Install-Ubuntu-Linux-Step-32.jpg)
2. 엔터 누르지 말고 `e` 키 입력, 그러면 아래와 같은 설정창 확인 가능.
   * ![](https://user-images.githubusercontent.com/8021479/146155593-32fb4ca5-1d39-4f51-a585-4b21a1e167f5.png)
3. `linux` 항목 가장 끝에 ~~ `quiet splash ---`  내용을 `quiet splash nomodeset ---` 으로 변경
   * `nomodeset` 추가
4. 변경 후 ctrl-x 나 F10 키를 누르면 바로 적용되어 재시동 된다.


이후는 부팅 후에 우분투 설치 내용



---

[다시 # Home main 으로](../README.md)
