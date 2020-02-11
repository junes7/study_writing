# Virtual Machine 설치하기

## 이것이 리눅스다 교제

* 설치경로: 

  김샘자바 → IoT커넥티드 카 → 빅데이터 → 다운로드 경로 → https://www.centos.org → Get Centos now  → CentOS Linux DVD ISO 이러면 미러 버전을 다운받을 수 있다

* 이전버전을 쓸거면 CentOS 7 말고 6버전을 사용할 것

alternative downloads →  base Distribution → 

![image-20200211094332628](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211094332628.png)

그리고 미러버전을 클릭하면 밑과 같이 나온다.

![image-20200211093200816](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211093200816.png)



그리고 

![image-20200211103917688](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211103917688.png)

이 버전을 다운로드 받는다

* VMware 다운로드 하는 방법

김샘자바  → IoT커넥티드 카 → 빅데이터 → [**https://www.vmware.com/**](https://www.vmware.com/) → 다운로드 → 무료 제품 다운로드 → Workstation Player → Windows용 Worksatation 15.5 player 사용해 볼 것

램은 최소한 16GB 정도 필요하다

window키 + pause break키 누르면 시스템 설정 상황이 나온다

* VMware 설치하는 방법(vmware player 15.5.1)

  

   ![image-20200211110208872](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211110208872.png)

  

 → 

![image-20200211110546716](C:\Users\wnstj\AppData\Roaming\Typora\typora-user-images\image-20200211110546716.png)

 → 

![image-20200211110646387](C:\Users\wnstj\AppData\Roaming\Typora\typora-user-images\image-20200211110646387.png)

 → 

![image-20200211110722634](C:\Users\wnstj\AppData\Roaming\Typora\typora-user-images\image-20200211110722634.png)

 → 

![image-20200211110929643](C:\Users\wnstj\AppData\Roaming\Typora\typora-user-images\image-20200211110929643.png)

 → 

![image-20200211110949590](C:\Users\wnstj\AppData\Roaming\Typora\typora-user-images\image-20200211110949590.png)

 → 

 → 





C:\Program Files (x86)\VMware\VMware Player vmware의  →  홈 디렉토리가 여기이다.



![image-20200211104013771](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211104013771.png)

vmware 기본 설정 실행하고 continue 누를 것

![image-20200211104101235](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211104101235.png)

VMware 기본 홈 화면이다



![image-20200211104254589](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211104254589.png)

이렇게 해서 new virtual 머신을 선택한다.

![image-20200211104418588](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211104418588.png)

그러면 이 화면이 뜨는데 '나는 나중에 설치할게'를 선택해준다.

라즈베리 파이에 설처되어 있는것이 debian이다

![image-20200211104646692](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211104646692.png)

그리고 centOS7 64비트를 선택해준다

![image-20200211104835766](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211104835766.png)

위의 virtual machine name은 내가 그냥 주는 이름이다. 근데 hadoop머신 4개 사용할 것이기 때문에 이름을 hadoop01이라고 설정해주었다.

 ![image-20200211105159430](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211105159430.png)

그리고 추천하는 디스크 사양인 20GB를 맞춰주고 하나의 파일로 저장하는 것을 선택해준다.

![image-20200211105321265](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211105321265.png)

여기서 VM머신의 설정을 해줄 수 있다.

C:\Users\student\Documents\Virtual Machines\hadoop01 여기가 중요한 설정 경로이고 이 안에 파일들이 다음과 같이 구성되어 있다.

![image-20200211105452548](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211105452548.png)



hadoop은 master slave 구조이다.

alt printscreen하면 capture할 수 있다.

ctrl + alt하면 마우스가 나온다

![image-20200211111813550](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211111813550.png)



상단 위 x표 누르고 suspend 상태로 종료하면 켜져있는 상태로 종료된다. 그래서  완전히 끄려면 suspend가 아니라 power off 로 종료시켜 주어야 한다.





![image-20200211112151518](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211112151518.png)

위와같이 remove from the library를 선택하면 machine을 라이브러리에서 제거할 수 있다.

open경로에서 경로 머신을 찾는다.

![image-20200211112239685](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211112239685.png)



라이브러리에서 제거한 파일을 다시 추가하려면 다음과 같이 열어서 추가시킨다.

cmd에서 ip확인 시 ipconfig명령어를 사용한다

![image-20200211112600532](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211112600532.png)

위와같이 ip가 할당되어 있다.

3번째 대역폭에 넣어줄 ip는 임으로 가지고 온다.

동적으로 ip를 할당할 때 가끔 4번째 ip가 바뀔 수 있다.

헷갈리는 부분이 있다

p68 

![image-20200211113914545](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211113914545.png)

이런 에러가 발생하는 이유: 이런 ip설정 모듈을 지원해주지 않는다.

그래서 vmnetcfg.exe파일을 복사해서 C:\Program Files (x86)\VMware\VMware Player 이 폴더 안에 넣어준다.





NAT 기술이 나온다.

![image-20200211114409496](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211114409496.png)

VMnet8 선택 후 change settings를 선택한 후 세번째 ip만 111로 바꿔준다.

![image-20200211114514355](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211114514355.png)

그럼 아래와 같이 아이피가 바뀌어 있는 것을 확인할 수 있다.



하둡의 버전들이 1.x 2.x 3.x 버전들이 있는데 이 중에 1.x버전을 사용하는 곳들도 있다.

4대의 hadoop머신을 구성해 설치한 후에 클러스터링을 한 후에 프로그램을 설치해준다.

HDFS 저장소

MapReduce 처리

host



![image-20200211133407434](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211133407434.png)

이 파일 용량이 4.5GB가 되어야 한다.



![image-20200211133541815](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211133541815.png)

여기 경로에 한글 이름이 들어가면 안 된다.

![image-20200211133721025](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211133721025.png)

이 화면에서 하얀색이 포커스이다. centos7을 설치하기 위해 enter를 두 번 누른다.

![image-20200211133932917](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211133932917.png)

여기서 한국어를 선택해주고 계속 진행해준다.

![image-20200211134046061](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211134046061.png)

키보드 레이아웃 미국 선택해주소 추가해준다.

![image-20200211134135666](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211134135666.png)

영어(미국) 선택해주고 화살표 Λ 이 버튼을 눌러 우선순위를 올려준다.

![image-20200211134234019](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211134234019.png)

소프트웨어 선택에서 '개발 및 창조를 위한 워크스테이션'을 선택해주고 완료 버튼을 눌러준다.

![image-20200211134348951](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211134348951.png)

네트워크 &호스트 이름에서 이더넷을 '끔'에서 '켬'으로 바꿔준다.

![image-20200211134454287](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211134454287.png)



![image-20200211134724320](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211134724320.png)

세개가 같이 설정되어야 한다. 그리고 완료 버튼을 눌러준다.

![image-20200211134748029](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211134748029.png)

그리고 수동으로 파티션 설정에서 표준 파티션을 설정해준다.

jps명령어가 잘 작동될 때까지 잘 집중하여야 한다.



![image-20200211135134834](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211135134834.png)

swap 메모리는 원래 RAM의 2배 정도로서 설정해야 하지만 지금은 

마운트 지점은 swap 용량은 2g로 설정해준다.

그리고 /는 용량을 설정 안 해줘도 자동 설정되기 때문에 추가해주고 아래와 같이 완료 버튼을 누르면 아래와 같이 나오는데 변경사항 적용해준다.

swap은 가상메모리이다.

![image-20200211135420024](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211135420024.png)



![image-20200211135443141](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211135443141.png)



![image-20200211135507021](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211135507021.png)

그러면 아래와 같이 설치가 시작된다.

![image-20200211140958167](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211140958167.png)

그러면 위와 같은 화면이 뜬다. 

ROOT암호는 bigdata를 넣어준다.

![image-20200211141235385](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211141235385.png)

사용자 생성은 성명도 hadoop 암호도 hadoop으로 설정해준다.

![image-20200211141432497](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211141432497.png)

그 다음 재부팅 해주고 관리자 계정으로 들어간다.

관리자 계정 root 비밀번호 hadoop

가상머신이름: hadoop02

ram: 1GB

harddisk: 20GB



![image-20200211155307326](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211155307326.png)

앞에 순서가 계정 @ host명 홈 디렉토리

​					root@localhost ~ 

root는 계정명 | localhost는 host명 | ~은 홈 디렉토리

shell prompt

[root@localhost ~]# su - hadoop
[hadoop@localhost ~]

$ 
[hadoop@localhost ~]$ su -
암호:
마지막 로그인: 화  2월 11 23:48:57 KST 2020 일시 :0
[root@localhost ~]# 



$가 붙어있는 것이 일반 계정이다.

''#''이 붙이었는 것이 관리자 계정이다. 

ls가 리스트 출력이다.





![image-20200211162619431](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211162619431.png)

이게 root가 사용하고 있는 홈 디렉토리이다.

![image-20200211162719871](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211162719871.png)

* home(홈디렉토리): 특정 계정으로 로그인 했을 때 자동으로 위치하는 폴더

  ​	모든 계정은 홈디렉토리를 갖고 있다.

  ​	기본 설정은 홈디렉토리명이 계정명과 동일								

  ​	root의 홈디렉토리명 root폴더

  root계정 => 프롬프트 #  /root

  일반계정 => 프롬프트 $ 

  ![image-20200211163602403](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211163602403.png)

su - : 사용자 계정으로부터 관리자 계정으로 전환할 때

su - hadoop: 관리자 계정으로부터 사용자 계정으로 전환할 때

ls: 파일 리스트 출력할 때

리눅스는 체계가 계정으로 관리된다. 거의 대부분의 회사 시스템이 리눅스 베이스이다. 규모가 큰 프로젝트들은 이런것만 가지고도 관리할 수 있다.

[계정 @ host명 현재 접속중인 폴더 ~] #: root $: 일반계정

root는 계정명 | localhost는 host명 | ~은 홈 디렉토리

/home/계정명

[root@localhost /]# cd ~
[root@localhost ~]# cd /

cd ~ 홈 디렉토리로 접근 cd / 루트 디렉토리로 접근

리눅스에서 사용하는 모든 리소스는 권한이 부여된다.

일반계정에서 사용할 수 없다.

[root@localhost ~]# cd /
[root@localhost /]# ls
bin   dev  home  lib64  mnt  proc  run   srv  tmp  var
boot  etc  lib   media  opt  root  sbin  sys  usr
[root@localhost /]# cd ~
[root@localhost ~]# ls
anaconda-ks.cfg       공개      문서      비디오  서식
initial-setup-ks.cfg  다운로드  바탕화면  사진    음악



[root@localhost ~]# su - hadoop
마지막 로그인: 수  2월 12 01:24:53 KST 2020 일시 pts/0
[hadoop@localhost ~]$ ls



* etc폴더는 각 종 설정파일을 보관하는 곳이다.

-시스템 및 프로그램의 환경설정 파일

-계정 파일, 네트워크 설정 파일 등 시스템의 주요 관리 파일

-백업 필요하다.

* usr폴더는 윈도우로 치면 program files와 비슷하다.

* dev폴더는 장치들이 위치하는 폴더이고 시스템의 모든 장치를 파일로 표현해 놓은 곳이다.
* 디렉토리 만들기: mkdir test
* 현재 폴더의 상위 폴더로 올라가기: cd ..
* 최상위 폴더로 가기: cd /
* 홈 디렉토리 폴더로 가기: cd ~
*  







































 

































 

