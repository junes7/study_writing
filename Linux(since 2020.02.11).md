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

![image-20200211110546716](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211110546716.png)

 → 

![image-20200211110646387](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211110646387.png)

 → 

![image-20200211110722634](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211110722634.png)

 → 

![image-20200211110929643](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211110929643.png)

 → 

![image-20200211110949590](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200211110949590.png)

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

하둡 저장 

하둡 처리 MapReduce

host

namenode - secondary name



secondary name load 로서 hadoop02를 정의해준다.



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

* 빅데이터 플랫폼을 구축하기 위한 준비작업

  3. 가상머신 복제하기
    
     -가상머신이 네 대 있다 가정하고 네 개의 가상머신을 만들어준다.
  
     * player 안에는 가상머신 복제기능이 없다.
   * C:\Users\student\Documents\Virtual Machines 이 안에 들어가서 hadoop1 폴더 카피한다
  

![image-20200212093955033](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200212093955033.png)

  

  * 여기서 i move it을 누르면 원래 파일이 가지고 있던 ip를 그대로 가져오고 I copied it 을 눌러야 새로운 ip를 할당받아온다.





![image-20200212094510371](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200212094510371.png)

![image-20200212094329684](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200212094329684.png)



이  리눅스 시스템을 부팅했을때 유선 연결됨이 올라오지 않는다면 유선 네트워크 설정으로 가서 저 위 베어링 같은 설정 버튼을 누르고 아래 그림의 자동으로 연결을 체크해준다. 그리고 적용버튼을 눌러서 부팅될 때 적용될 수 있도록 해준다.

* 하둡은 가상머신 4대가 하나의 서버처럼 사용된다.
  * 각 머신마다 고유의 고정 ip를 가지고 있어야 한다.

-ip확인 

[root@localhost ~]# ifconfig

이렇게 확인해준다.

hadoop1: 192.168.111.132
hadoop2: 192.168.111.131
hadoop3: 192.168.111.130
hadoop4: 192.168.111.128



![image-20200212111352822](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200212111352822.png)

* 다음과 같이 화면 잠금을 꺼주면 된다.

4. 하둡 서버를 구축하기 위한 클러스터링 설정하기

   * 원격 접속 확인 방법

     [root@localhost ~]# ssh 192.168.111.128
     The authenticity of host '192.168.111.128 (192.168.111.128)' can't be established.
     ECDSA key fingerprint is SHA256:1rj0b88qwaKsPhipxSQmsToBiaMMTng6j3sodFx4/4o.
     ECDSA key fingerprint is MD5:71:a5:e3:fc:62:6e:69:cf:8a:f9:b1:e7:a5:7f:d2:c8.
     Are you sure you want to continue connecting (yes/no)? yes
     Warning: Permanently added '192.168.111.128' (ECDSA) to the list of known hosts.
     root@192.168.111.128's password: 
     Last login: Wed Feb 12 19:36:32 2020
     ABRT에 의해 '2' 건의 문제가 발견되었습니다. (다음을 실행하여 보다 자세한 내용을 확인합니다: abrt-cli list --since 1581502829
     [root@localhost ~]# exit
     logout
     Connection to 192.168.111.128 closed.

     * 위의 exit이 로그아웃 명령어이다.

     * 위의 ssh 192.168.111.128이 telnet포트를 암호화 한 후 접속한 것이다. 접속 포트 22번이다. (telnet은 23번이다.)

       

   ![image-20200212112515321](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200212112515321.png)

   sts에서 다음과 같이 하여 remote system explorer를 열어준다.

   ![image-20200212112637017](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200212112637017.png)

   

   ※ host-only vs NAT vs bridge

   * host only

   -guest PC를 하나로 묶어 인터넷 통신되게 만드는 것

   -HOST는 공유기를 통해 인터넷에 접근한다.

   * NAT

   -

   -

   bridge

   

   

    

   -방화벽해제

   * host명 변경 방법

   h+tab을 주면 자동완성된다.

   hostnamectl set-hostname hadoop01

   hostnamectl set-hostname hadoop02

   

   host명인 localhost를 hadoop01로 변경해준다.

   host명인 localhost를 hadoop02로 변경해준다.

   확인할 때

   [root@localhost ~]# hostname

   하면 바뀐 호스트네임을 확인할 수 있다.

   그리고 터미널 닫고 다시 열으면 다음과 같이 바뀌어 있다.

   [root@localhost ~]#

   여기에

   [root@localhost ~]#hostnamectl set-hostname hadoop01

   넣으면

   [root@hadoop01 ~]# 이렇게 바뀌어 있다

   

   * 바뀐 호스트네임 원격접속으로 확인한다.

   [root@hadoop01 ~]# ssh 192.168.111.131
   root@192.168.111.131's password: 
   Last login: Wed Feb 12 20:14:46 2020 from 192.168.111.132
   [root@hadoop02 ~]# exit
   logout
   Connection to 192.168.111.131 closed.
   [root@hadoop01 ~]# ssh 192.168.111.130
   root@192.168.111.130's password: 
   Permission denied, please try again.
   root@192.168.111.130's password: 
   Last failed login: Wed Feb 12 22:31:22 KST 2020 from 192.168.111.132 on ssh:notty
   There was 1 failed login attempt since the last successful login.
   Last login: Wed Feb 12 20:17:17 2020 from 192.168.111.132
   [root@hadoop03 ~]# exit
   logout
   Connection to 192.168.111.130 closed.
   [root@hadoop01 ~]# ssh 192.168.111.128
   root@192.168.111.128's password: 
   Last login: Wed Feb 12 20:17:37 2020 from 192.168.111.132
   [root@hadoop04 ~]# exit
   logout
   Connection to 192.168.111.128 closed.
   [root@hadoop01 ~]# 

   

   

![image-20200212133923614](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200212133923614.png)



[root@hadoop01 ~]# systemctl list-units --type=service

실행 중인 서비스 보기

실행 중인 모든 서비스 목록을 보려면 위와 같이 명령어를 준다.

현재의 모든 서비스들을 보여준다.

![image-20200212134337155](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200212134337155.png)



끝까지 가면 ctrl c 눌러서 밖으로 나와준다.

systemctl은 7버전부터 시스템 관리할 때 사용하는 명령어 이전 버전은 service를 사용하였다.



[root@hadoop01 ~]# systemctl status firewalld
● firewalld.service - firewalld - dynamic firewall daemon
   Loaded: loaded (/usr/lib/systemd/system/firewalld.service; enabled; vendor preset: enabled)
   Active: active (running) since 수 2020-02-12 19:21:30 KST; 3h 22min ago
     Docs: man:firewalld(1)
 Main PID: 1117 (firewalld)
    Tasks: 2
   CGroup: /system.slice/firewalld.service
           └─1117 /usr/bin/python2 -Es /usr/sbin/firewalld --nofork --nopid

 2월 12 19:21:28 localhost.localdomain systemd[1]: Starting firewalld - dynamic firewall.....
 2월 12 19:21:30 localhost.localdomain systemd[1]: Started firewalld - dynamic firewall ...n.
Hint: Some lines were ellipsized, use -l to show in full.
[root@hadoop01 ~]# systemctl stop firewalld
[root@hadoop01 ~]# systemctl status firewalld
● firewalld.service - firewalld - dynamic firewall daemon
   Loaded: loaded (/usr/lib/systemd/system/firewalld.service; enabled; vendor preset: enabled)
   Active: inactive (dead) since 수 2020-02-12 22:45:45 KST; 13s ago
     Docs: man:firewalld(1)
  Process: 1117 ExecStart=/usr/sbin/firewalld --nofork --nopid $FIREWALLD_ARGS (code=exited, status=0/SUCCESS)
 Main PID: 1117 (code=exited, status=0/SUCCESS)

 2월 12 19:21:28 localhost.localdomain systemd[1]: Starting firewalld - dynamic firewall.....
 2월 12 19:21:30 localhost.localdomain systemd[1]: Started firewalld - dynamic firewall ...n.
 2월 12 22:45:44 hadoop01 systemd[1]: Stopping firewalld - dynamic firewall daemon...
 2월 12 22:45:45 hadoop01 systemd[1]: Stopped firewalld - dynamic firewall daemon.
Hint: Some lines were ellipsized, use -l to show in full.

현재시점으로 방화벽이 꺼졌다고 상황이 출력된다.

[root@hadoop01 ~]#reboot

명령어를 쳐서 재부팅시킨다.

system kernel설정에 의해 방화벽이 다시 올라가 있다 그래서 아래의 명령어로 방화벽이 불가능하게 만든 다음에 상황을 살피고 다시 리부팅 시킨다.

[root@hadoop01 ~]# systemctl disable firewalld
Removed symlink /etc/systemd/system/multi-user.target.wants/firewalld.service.
Removed symlink /etc/systemd/system/dbus-org.fedoraproject.FirewallD1.service.
[root@hadoop01 ~]# systemctl stop firewalld
[root@hadoop01 ~]# systemctl status firewalld
● firewalld.service - firewalld - dynamic firewall daemon
   Loaded: loaded (/usr/lib/systemd/system/firewalld.service; disabled; vendor preset: enabled)
   Active: inactive (dead)
     Docs: man:firewalld(1)

 2월 12 22:51:16 hadoop01 firewalld[3374]: WARNING: COMMAND_FAILED: '/usr/sbin/iptables -w10...?).
 2월 12 22:51:16 hadoop01 firewalld[3374]: WARNING: COMMAND_FAILED: '/usr/sbin/iptables -w10...me.
 2월 12 22:51:16 hadoop01 firewalld[3374]: WARNING: COMMAND_FAILED: '/usr/sbin/iptables -w10...me.
 2월 12 22:51:16 hadoop01 firewalld[3374]: WARNING: COMMAND_FAILED: '/usr/sbin/iptables -w10...?).
 2월 12 22:51:16 hadoop01 firewalld[3374]: WARNING: COMMAND_FAILED: '/usr/sbin/iptables -w10...?).
 2월 12 22:51:16 hadoop01 firewalld[3374]: WARNING: COMMAND_FAILED: '/usr/sbin/iptables -w10...?).
 2월 12 22:51:16 hadoop01 firewalld[3374]: WARNING: COMMAND_FAILED: '/usr/sbin/iptables -w10...?).
 2월 12 22:51:16 hadoop01 firewalld[3374]: WARNING: COMMAND_FAILED: '/usr/sbin/iptables -w10...?).
 2월 12 22:51:46 hadoop01 systemd[1]: Stopping firewalld - dynamic firewall daemon...
 2월 12 22:51:46 hadoop01 systemd[1]: Stopped firewalld - dynamic firewall daemon.
Hint: Some lines were ellipsized, use -l to show in full.
[root@hadoop01 ~]#  reboot

![image-20200212141742119](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200212141742119.png)

여기 있는 내용을 다 삭제해준다.

192.168.111.132 hadoop01
192.168.111.131 hadoop02
192.168.111.130 hadoop03
192.168.111.128 hadoop04

그리고 위의 내용을 채워주고 저장해준다.

그러나 혹시 reboot로 인해서 ip주소가 바뀌었으면 위의 작업을 다시 해 주어야 한다.

<<빅데이터 플랫폼 구축>>

* 1. vmware 설치
* 2. 머신생성 - centos7

* 3. 머신복제

  -ip확인

* 4. 머신 4대(CentOS)를 클러스터링

-방화벽해제

-hostname변경

-DNS설정하는 작업 => 하위 순서로 들어가는 것

*hosts파일 등록

*네트워크 프로세스를 restart

*설정확인 - 설정을 성공 완료했는지 확인해줄 것

*네 대에 모두 적용이 되도록

--hadoop01머신에서 hadoop02,  hadoop03,  hadoop04에 직접 접속할 것

 [root@hadoop01 ~]# /etc/init.d/network restart
Restarting network (via systemctl):                        [  OK  ]
[root@hadoop01 ~]# ssh hadoop02
The authenticity of host 'hadoop02 (192.168.111.131)' can't be established.
ECDSA key fingerprint is SHA256:gWYbrhoXfz91Nnvc19vRk59IGurW/N4RJlN8J6dm1m0.
ECDSA key fingerprint is MD5:f4:7c:e3:c6:57:17:11:1e:95:3b:7d:fd:55:e2:04:4d.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'hadoop02' (ECDSA) to the list of known hosts.
root@hadoop02's password: 
Last login: Wed Feb 12 23:14:14 2020 from 192.168.111.132
[root@hadoop02 ~]# 

그러고 나면 위와 같이 hadoop01에서 다른 머신으로접속이 가능하다.

[로컬 저장소로 copy]

[원격 서버로 copy]

```bash
//scp copy할 파일(위치까지 명시) copy받을 서버의 위치

scp    /etc/hosts 	root@hadoop02:/etc/hosts

----    ---------   -----------------------
명령어   copy할 파일   target서버의 위치와 파일명
```

[원격 서버에 실행명령]

```javascript
//ssh 서버 "실행할명령문
      ---
      ip, domain
```

* 확인작업

[root@hadoop01 ~]# scp /etc/hosts root@hadoop02:/etc/hosts
root@hadoop02's password: 
hosts                              100%  100    46.5KB/s   00:00    
[root@hadoop01 ~]# ssh hadoop02
root@hadoop02's password: 
Last login: Wed Feb 12 23:29:47 2020 from 192.168.111.132
[root@hadoop02 ~]# exit
logout
Connection to hadoop02 closed.
[root@hadoop01 ~]# ssh hadoop02 "/etc/init.d/network restart"
root@hadoop02's password: 
Restarting network (via systemctl):  [  OK  ]
[root@hadoop01 ~]# ssh hadoop02
root@hadoop02's password: 
Last login: Wed Feb 12 23:45:05 2020 from hadoop01
[root@hadoop02 ~]# ssh hadoop03
The authenticity of host 'hadoop03 (192.168.111.130)' can't be established.
ECDSA key fingerprint is SHA256:1rj0b88qwaKsPhipxSQmsToBiaMMTng6j3sodFx4/4o.
ECDSA key fingerprint is MD5:71:a5:e3:fc:62:6e:69:cf:8a:f9:b1:e7:a5:7f:d2:c8.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'hadoop03,192.168.111.130' (ECDSA) to the list of known hosts.
root@hadoop03's password: 
Last login: Wed Feb 12 23:31:04 2020 from 192.168.111.132
[root@hadoop03 ~]# exit
logout
Connection to hadoop03 closed.
[root@hadoop02 ~]# exit
logout
Connection to hadoop02 closed.

* 암호화된 통신을 위해서 공개키생성 후 배포한다.

  우리는 하둡 실행을 하둡 계정에서 실행할 것이다.

  -암호화된 통신을 위해서 

  xwindow가 GUI(그래픽 유저 환경)를 뜻한다.

* 현재 hadoop 계정의 루트 폴더에 들어와 있다.

* 숨김파일 보이기 체크 해제해준다.
* 

remote remote

4. -네트워크 설정

   -DNS 설정

```bash
[root@hadoop01 ~]# su hadoop
[hadoop@hadoop01 root] cd ~
[hadoop@hadoop01 ~] ssh hadoop02
The authenticity of host 'hadoop02 (192.168.111.131)' can't be established.
ECDSA key fingerprint is SHA256:gWYbrhoXfz91Nnvc19vRk59IGurW/N4RJlN8J6dm1m0.
ECDSA key fingerprint is MD5:f4:7c:e3:c6:57:17:11:1e:95:3b:7d:fd:55:e2:04:4d.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'hadoop02,192.168.111.131' (ECDSA) to the list of known hosts.
hadoop@hadoop02's password: 
Permission denied, please try again.
hadoop@hadoop02's password: 
Last failed login: Thu Feb 13 00:21:31 KST 2020 from hadoop01 on ssh:notty
There was 1 failed login attempt since the last successful login.
[hadoop@hadoop02 ~] exit
logout
Connection to hadoop02 closed.
[hadoop@hadoop01 ~] ssh-keygen -t rsa
Generating public/private rsa key pair.
Enter file in which to save the key (/home/hadoop/.ssh/id_rsa): 
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/hadoop/.ssh/id_rsa.
Your public key has been saved in /home/hadoop/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:nFzQRjfC8s7ZUp5UCRiR7ke4Pmfr4uLo5MWlUjoZ/SE hadoop@hadoop01
The key's randomart image is:
+---[RSA 2048]----+
|        .+==+. . |
|        ..*o .o  |
|         =.. .   |
|       + o+ +    |
|      . E+oO .   |
|       * =B.=    |
|      * +..o     |
|     o =. + o    |
|     .+..o.*o.   |
+----[SHA256]-----+

[hadoop@hadoop01 ~] cd .ssh
[hadoop@hadoop01 .ssh] ls
id_rsa  id_rsa.pub  known_hosts
[hadoop@hadoop01 .ssh]$ ssh-copy-id -i id_rsa.pub hadoop@hadoop02
/usr/bin/ssh-copy-id: INFO: Source of key(s) to be installed: "id_rsa.pub"
/usr/bin/ssh-copy-id: INFO: attempting to log in with the new key(s), to filter out any that are already installed
/usr/bin/ssh-copy-id: INFO: 1 key(s) remain to be installed -- if you are prompted now it is to install the new keys
hadoop@hadoop02's password: 

Number of key(s) added: 1

Now try logging into the machine, with:   "ssh 'hadoop@hadoop02'"
and check to make sure that only the key(s) you wanted were added.

[hadoop@hadoop01 .ssh]$


```



ssh hadoop02했을때 비밀번호를 묻지 말아야 한다.

```bash
[hadoop@hadoop01 .ssh]$ ssh hadoop03
Last login: Thu Feb 13 00:33:03 2020 from hadoop01
[hadoop@hadoop03 ~]$ ssh hadoop04
The authenticity of host 'hadoop04 (192.168.111.128)' can't be established.
ECDSA key fingerprint is SHA256:1rj0b88qwaKsPhipxSQmsToBiaMMTng6j3sodFx4/4o.
ECDSA key fingerprint is MD5:71:a5:e3:fc:62:6e:69:cf:8a:f9:b1:e7:a5:7f:d2:c8.
Are you sure you want to continue connecting (yes/no)? no
Host key verification failed.
[hadoop@hadoop03 ~]$ exit
logout
Connection to hadoop03 closed.
[hadoop@hadoop01 .ssh]$ ssh hadoop04
Last failed login: Thu Feb 13 00:35:02 KST 2020 from hadoop01 on ssh:notty
There were 2 failed login attempts since the last successful login.
Last login: Wed Feb 12 01:52:20 2020
[hadoop@hadoop04 ~]$ exit
logout
Connection to hadoop04 closed.
[hadoop@hadoop01 .ssh]$ ssh hadoop02
Last login: Thu Feb 13 00:21:35 2020 from hadoop01
[hadoop@hadoop02 ~]$ exit
logout
Connection to hadoop02 closed.
[hadoop@hadoop01 .ssh]$ ssh hadoop03
Last login: Thu Feb 13 00:36:19 2020 from hadoop01
[hadoop@hadoop03 ~]$ exit
logout
Connection to hadoop03 closed.
[hadoop@hadoop01 .ssh]$ ssh hadoop04
Last login: Thu Feb 13 00:36:45 2020 from hadoop01
[hadoop@hadoop04 ~]$ exit
logout
Connection to hadoop04 closed.
[hadoop@hadoop01 .ssh]$ history
```

4. keygen



5. 각종 프로그램 설치

   -SSH 프로토콜 설정

   -hadoop을 테스트하기 위해서는 자바가 반드시 필요하므로 

   -java, hadoop을 설치하고 설정을 한 후 테스트한다.

   * JDK 설치 및 설정

   window에서 setup하는거랑 동일한 작업을 할 것이다.

   https://www.oracle.com/j2se/

   java.sun.com/j2se/

   ​	https://www.oracle.com/java/technologies/javase/javase8u211-later-archive-downloads.html

   

   ![image-20200213095612860](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200213095612860.png)

   linux-x64.rpm은 setup.exe같은 버전이고 linux-x64.tar.gz는 zip파일같은 압축 버전이다.

   ```bash
   [root@hadoop01 ~]# ls
   anaconda-ks.cfg       jdk-8u231-linux-x64.rpm  다운로드  바탕화면  사진  음악
   initial-setup-ks.cfg  공개                     문서      비디오    서식
   [root@hadoop01 ~]# rpm -Uvh jdk-8u231-linux-x64.rpm 
   ```

   https://www.lesstif.com/pages/viewpage.action?pageId=7635004

   ls: list 출력 명령어

   -U:  --upgrade 패키지 업그레이드

   -v: verbose 자세한 정보 출력

   -h: print hash marks: 설치 진행 상황을 #문자를 이용하여 출력한다.

   /usr/java/dk1.8.0_231-amd64에 설치되었다.

   

   ![image-20200213102646760](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200213102646760.png) 

   

**지금부터 할 일

-hadoop02, hadoop03, hadoop04에 jdk설치 



하둡 설치파일 다운로드

http://apache.org/ 

사이트 접속

→

![image-20200213111510123](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200213111510123.png)

→

![image-20200213111546372](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200213111546372.png)

→

![image-20200213111636954](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200213111636954.png)



bin.tar.gz는 빈 파일만 들어가 있는거고 tar.gz는 소스 파일도 포함되어 있는 압축 파일이다.

![image-20200213112508870](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200213112508870.png)

여기 소유자 계정이 hadoop인 이유는 복사할때 hadoop계정인 곳으로 복사해 주었기 때문에 이렇게 권한이 뜬다.

* 압축풀기 방법

* 사용방법

$ tar -cvzf [압축한 파일 이름] [압축할 파일이나 폴더명]

-해당 경로의 모든 파일을 xxx.tar.gz로 압축

$ tar -cvzf xxx.tar.gz *

-권한없는 파일 패스하며, 해당 경로의 모든 파일을  xxx.tar.gz로 압축

$ tar -cvzf xxx.tar.gz  * --ignore-failed-read

옵션  		설치

| -c   | 새로운 tar 파일 생성                           |
| ---- | ---------------------------------------------- |
| -x   | 기존의 tar파일의 압축을 풀어주겠다는 의미이다  |
| -v   | 명령어 실행 시 과정을 화면에 출력해준다.       |
| -x   | 기존의 tar파일의 압축을 풀어주겠다는 의미이다. |
| -z   | gzip사용                                       |
| -p   | 퍼미션 포함                                    |
| -f   | 파일의 이름을 지정                             |
| -z   | gzip사용                                       |

[hadoop@hadoop01 ~]$ tar -zxvf hadoop-1.2.1.tar.gz 

위 명령어로 압축 풀어준다.

[hadoop@hadoop01 ~]$ scp /home/hadoop/hadoop-1.2.1.tar.gz hadoop@hadoop02:/home/hadoop/



hadoop02홈에 들어가면 복사 잘 되어있는 것을 확인할 수 있다.



Su hadoop

[hadoop@hadoop01 ~]$ tar -zxvf hadoop-1.2.1-bin.tar.gz

ssh hadoop02 "tar -zvxf hadoop-1.2.1-bin.tar.gz"

ssh hadoop04 "tar -zxvf hadoop-1.2.1.tar.gz" 

 .sh는 shell파일이다.



mapreduce-site.xml
jobtracker(일을 명령할(시킬) 컴퓨터의 주소)에 대한 정보이다.





slave는 데이터와 테스크 로드의 경로이다.





scp /home/hadoop/hadoop-1.2.1/conf/* hadoop@hadoop03:/home/hadoop/hadoop-1.2.1/conf

 /home/hadoop/hadoop-1.2.1/bin/hadoop namenode -format

```bash
//conf설정을 hadoop02설정 폴더로 넘겨주는 작업
[hadoop@hadoop01 ~]$ scp /home/hadoop/hadoop-1.2.1/conf/* hadoop@hadoop02:/home/hadoop/hadoop-1.2.1/conf
//hadoop 초기 설정해주는 것?
[hadoop@hadoop01 ~]$ /home/hadoop/hadoop-1.2.1/bin/hadoop namenode -format
//hadoop프로그램 시작
[hadoop@hadoop01 ~]$ /home/hadoop/hadoop-1.2.1/bin/start-all.sh
//hadoop프로그램 종료
[hadoop@hadoop01 ~]$ /home/hadoop/hadoop-1.2.1/bin/stop-all.sh
//다른 하둡 서버가 잘 실행 되는지 확인
[hadoop@hadoop01 ~]$ ssh hadoop02 "jps"
//자기 자신이 잘 실행되는지 확인
[hadoop@hadoop01 hadoop-1.2.1]$ jps
54340 JobTracker
54550 Jps
54154 NameNode

//하둡의 /input안 리스트 출력
[hadoop@hadoop01 hadoop-1.2.1]$ /home/hadoop/hadoop-1.2.1/bin/hadoop fs -ls /input
Found 1 items
-rw-r--r--   3 hadoop supergroup       1366 2020-02-14 00:43 /input/README.txt
//하둡 안의 /input 폴더 삭제
[hadoop@hadoop01 hadoop-1.2.1]$ /home/hadoop/hadoop-1.2.1/bin/hadoop fs -rmr /input
Deleted hdfs://hadoop01:9000/input
//하둡 안에 /input 폴더 생성하기
[hadoop@hadoop01 hadoop-1.2.1]$ /home/hadoop/hadoop-1.2.1/bin/hadoop fs -mkdir /input
//하둡 안 /input안에 README.txt 파일 복사하기
[hadoop@hadoop01 hadoop-1.2.1]$ /home/hadoop/hadoop-1.2.1/bin/hadoop fs -copyFromLocal README.txt /input
//args[0]
//현재폴더 jar파일 안 wordcount클래스 검색저장할 //폴더 단어세기 from /input/README.txt to /output
[hadoop@hadoop01 hadoop-1.2.1]$ ./bin/hadoop jar hadoop-examples-1.2.1.jar wordcount /input/README.txt /output


```



![image-20200213153528389](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200213153528389.png)

* /input 밑에 무슨 파일이 있는지 확인할 때 사용하는 명령어

/home/hadoop/hadoop-1.2.1/bin/hadoop fs -ls /input

아니면 50070 접속해서 확인한다.

* /input 밑에 파일을 지울 때 사용하는 명령어

[hadoop@hadoop01 hadoop-1.2.1]$ /home/hadoop/hadoop-1.2.1/bin/hadoop fs -rmr /input
Deleted hdfs://hadoop01:9000/input

* 사용이 끝난 다음에는 반드시 꺼 주어야 한다. 그렇지 않으면 읽기 전용으로 전환되어서 다시 다 설정해주어야 한다.

오류를 찾을 때 namenode랑 jobtracker를 중심으로 찾는다.



http://hadoop01:50070/ 여기 들어가서 확인할 것!!!

이 부분의 word cloud 검색 결과이다.

![image-20200214105016722](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200214105016722.png)



5. hadoop의 EchoSystem을 살펴보고 EchoSystem을 설치하여야 한다.

hadoop-examples-1.2.1.jar의 wordcount를 이용해서 작업하기
-HDFS에 myinput폴더를 작성한다.
-LICENSE.txt를 복사한다.
-wordcount를 적용
-출력결과는 myoutput으로 작성할 것



* ip 바뀌었을 때
  * /etc/hosts
  * scp 모든 머신에 copy
  * 네트워크 프로세스 restart

* 빅데이터의 5대 요소(5V)

크기, 속도, 다양성, 정확성(가치), (정확한)값

volume, velocity, variety, veracity, value

sns 활동내역을 보고 harvard 입학 취소한 사례

=> 신중하게 sns를 사용할 것

빅데이터 뿐만 아니라 정형화 된 데이터는 정형화 된 채로 또 필요하다







포트폴리오 오늘 제출(금요일까지 업데이트해서 강사님한테 제출)

1,2번 어떤것을 기술했는지

3,4,번은 받은 데이터를 활용해서 어떻게 작업을 했었는지 기술해 줄 것

전체 프로젝트의 테이블 구성

나의 개발 부분

시스템 구조 그림 형식으로 설계

시스템 구축은 어떻게 어떻게 해서 설계했다.

maven 구성 mybatis 어떻게 연동



* 데이터 수집, 

IoT, 정형데이터, (RDBMS) - sqoop, (로그데이터(log)) - flume, (SNS, 웹페이지, 크롤링) - R

* 데이터 저장

HDFS, no-SQL

* 데이터 처리, 

데이터의 처리, MapReduce → R

* 데이터 분석, 

감정분석, 자연어처리, 키워드 분석, 패턴 분석, 데이터마이닝

ex) Text Mining, NLP, Real-time analysis, Batch analysis, Scalability

* 분석 결과 활용

시각화, 특정 기능의 Input데이터로 활용

ex) MongoDB

각종 chart라이브러리 D3



전자정부framework는 개발하는데 필요한 요소들을 하나의 패키지로 묶어놓은 것들이다.

아마존 AWS Microsoft Azure 

* 분석(이게 빅데이터의 기본 값)
  * HDFS에 저장
* RDBMS분석

UTF-8로 변경

tern 설치

블로그 install설치 데이터 툴 설치

글꼴수정



* HDFS에 적재하는 방법



[root@hadoop01 hadoop-1.2.1]# cd ..
[root@hadoop01 hadoop]# echo $LANG
ko_KR.UTF-8

[root@hadoop01 hadoop]# su hadoop

[hadoop@hadoop01 ~]$ cd hadoop-1.2.1/ 
[hadoop@hadoop01 hadoop-1.2.1]$ pwd (print working directory)

전체 경로를 보여달라는 명령어

/home/hadoop/hadoop-1.2.1
[hadoop@hadoop01 hadoop-1.2.1]$ ls

[hadoop@hadoop01 hadoop-1.2.1]$ /home/hadoop/hadoop-1.2.1/bin/hadoop fs -copyFromLocal NOTICE.txt /input

[hadoop@hadoop01 hadoop-1.2.1]$ ./bin/hadoop jar hadoop-examples-1.2.1.jar wordcount /input/NOTICE.txt /wordcount_output



* 하둡 stswork에서 할 일(정신 똑바로 차릴 것!!!!)

하둡은 그냥 자바프로젝트에서 작업한다.

new → java project

![image-20200217134041388](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200217134041388.png)

저렇게 프로젝트 생성하고 no를 눌러 끝내준다.



![image-20200217134201771](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200217134201771.png)

저런 경로를 따라서 가줄 것

그다음 buildpath addlibraries



![image-20200217141603035](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200217141603035.png)

이 파일을 ant라고 부른다.

무언가 변경될 때마다 build.xml을 실행시켜 주어야 한다.

![image-20200217145412766](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200217145412766.png)

여기 이 파일을 

![image-20200217145447484](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200217145447484.png)

여기로 옮겨줄 것!!!

[hadoop@hadoop01]$ ./hadoop-1.2.1/bin/hadoop jar multi-hadoop-examples.jar hdfs.exam.HDFSExam01 output.txt. hellohadoop



파일이 변경되면 build.xml부터 실행해준다.

[hadoop@hadoop01]$ ./hadoop-1.2.1/bin/hadoop jar multi-hadoop-examples.jar hdfs.exam.HDFSTest02 output.txt. 

hdfs에서 읽은 데이터: hellohadoop

build.xml이 필요한 설정 파일을 .jar로 묶어준다.



[hadoop@hadoop01]$ ./hadoop-1.2.1/bin/hadoop jar multi-hadoop-examples.jar hdfs.exam.HDFSTest02 /user/hadoop/output.txt. output1.txt 

#### 하둡의 목적

빅데이터를 저장하고 처리하는 목적이 있다.

* 처리방법: 맵리듀스(Map Reduce)

* 처리방법: HDFS이용(하둡이 가지고 있는 분산 파일 시스템)

HDFS

* hadoop fs -mkdir /input

* hadoop01:50070 페이지가 xwindow상에서 볼 수 있도록 만들어준 admin page이다.

* hadoop fs -copyFromLocal README.txt /input

input 폴더 안에 README.txt를 복사해서 넣어주는 명령어

프로그램 → 시스템 도구 →  설정 →  전원 →  절전 → 빈 화면 →  안함 으로 설정 해준다.

cd ~ 홈 디렉토리로 이동

cd / root 디렉토리로 이동(최상위 폴더)

pwd 현재 들어간 위치의 경로를 보여준다. 

linux상에서 shell script 파일들은 다 열어볼 수 있다.



/home/hadoop/hadoop-1.2.1/bin/start-all.sh

path(경로)를 걸어두지 않았기 때문에 내가 실행시키고 싶은 shell script 파일이 들어있는 전체 경로를 다 적어주어야 한다.



/home/hadoop/hadoop-1.2.1/bin/hadoop []

[]안에 들어갈 옵션

fs: hdfs안의 명령어를 묶어놓은 곳(분산 파일 시스템에 관한

jar: java파일 실행



./bin/hadoop jar ./hadoop-examples-1.2.1.jar wordcount



뒤에 명령행 매개변수가 있으면 적어주면 된다.



![image-20200219103540224](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200219103540224.png)

여기중 mapred(mapreduce)이고

dfs는 안에 data랑 namesecondary로서 secondarynamenode에 관한 폴더가 들어있다.

![image-20200219103853594](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200219103853594.png)

여기 data 폴더는 datanode에 관한 정보들이 들어있다.

![image-20200219104009331](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200219104009331.png)

여기는 폴더안에 .meta파일에 대한 정보도 제공해준다.

* 문제가 발생했을 때

하둡머신 1,2,3,4 돌면서

![image-20200219104225582](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200219104225582.png)



이 그림 안에 있는 폴더를 삭제해준다.

![image-20200219111442501](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200219111442501.png)

이렇게 해서 Quick Type Hierarchy로 들어간 다음에 설정을 해준다.

![image-20200219111219687](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200219111219687.png)



![image-20200219112259079](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200219112259079.png)



```bash
[hadoop@hadoop01 hadoop-1.2.1]$ ./bin/hadoop fs -rmr /input
Deleted hdfs://hadoop01:9000/input
[hadoop@hadoop01 hadoop-1.2.1]$ ./bin/hadoop fs -rmr /out
Deleted hdfs://hadoop01:9000/out
[hadoop@hadoop01 hadoop-1.2.1]$ ./bin/hadoop fs -rmr /wordcount_output
Deleted hdfs://hadoop01:9000/wordcount_output
//mapreduce 상에 필요없는 폴더들을 지워준다.

[hadoop@hadoop01 hadoop-1.2.1]$ ./bin/hadoop jar ../multi-hadoop-examples.jar hdfs.exam.HDFSCopyTest /user/hadoop/output.txt /copytest
//명령어를 root위치에 파일로 만들어진 부분에 해 둘 것이다

```





![image-20200219135207783](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200219135207783.png)

d는 폴더 - 은 파일을 의미한다. 그리고 rwx는 소유권한을 의미한다.



[root@exam ~]# cd mytest cd하고 mytest만 넣으면 뒤에 /가 자동으로 붙는다.



cp 로컬에서 파일 복사할 때 scp는 원격지로 파일 복사할 때 사용한다.





mytest1

​	+

​	|________________mytest2

​							+

​							|_________________mytest3

이렇게 만드는 방법

[root@exam mytest]# mkdir -p mytest1/mytest2/mytest3



[root@exam mytest]# rmdir mytest1
[root@exam mytest]# rm mytest1
rm: cannot remove `mytest1': 디렉터리입니다
[root@exam mytest]# rm -r mytest1
rm: descend into directory `mytest1'? y
rm: descend into directory `mytest1/mytest2'? y
rm: remove 디렉토리 `mytest1/mytest2/mytest3'? y
rm: remove 디렉토리 `mytest1/mytest2'? y
rm: remove 디렉토리 `mytest1'? y
[root@exam mytest]# rm -rf test
[root@exam mytest]# cd ~

root 홈디렉토리 hadooptest폴더 생성 후

cd 명령어를 이용하여 hadooptest로 이동한다.

-/etc/sysconfig폴더 copy하기

-/root/의 anaconda-ks.cfg파일 복사하기

-복사한 후 my_conda.cfg로 rename

-아래의 구조를 갖고 있는 서브 디렉토리 생성하기

mytest1

​	+

​	| ---------/etc/hosts 파일 복사

​	|________________mytest2

​							+

​							|_________________mytest3

-여기까지 캡쳐하기

-mytest2폴더 삭제하기

-캡쳐하기

-작업 완료 후 캡쳐된 파일 2개 메일로 전송하기

more my_conda.cfg

space는 다음 B는 앞 페이지로 이동한다.



![image-20200219152732656](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200219152732656.png)



#### 맵 리듀스(mapreduce) 

맵리듀스는 데이터를 분류하고 처리해주는 작업을 해준다.

mapper는 카테고리 분야별로 데이터를 나눠 처리해준다. 

job은 맵과 리듀스를 처리해주는 역할 -> Driver에 구현해 주었다.





#### 접속은 root로, 하둡 실행은 hadoop 계정으로







#### 맵퍼 설정하기







![image-20200219174959549](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200219174959549.png)



어느 분야를 가든지 spring framework는 중요하다.

프로세스가 떠있는 상황이면 점유되어 있는 상황이다.



하둡 서버상에서 문제가 생겼을 때 어떻게 해결을 해야 하는지를 알고 있어야 한다.



Tomcat Access log가 실행이 된다.

```bash
[hadoop@hadoop01 hadoop-1.2.1]$ ./bin/hadoop fs -mkdir /input
[hadoop@hadoop01 hadoop-1.2.1]$ ./bin/hadoop fs -put README.txt /input/
[hadoop@hadoop01 hadoop-1.2.1]$ ./bin/hadoop fs -ls /input/
//하둡 안에서 파일 시스템으로 값을 집어넣는 방법

[hadoop@hadoop01 hadoop-1.2.1]$ ./bin/hadoop jar hadoop-examples-1.2.1.jar wordcount /input/README.txt /output





```



hdfs를 관리하는 admin(관리자) 페이지



job을 관리하는 admin(관리자) 페이지



map이 끝나면 shuffle단계고, 이 작업이 끝나면 reduce 단계이다.



=>  mapred.basic과 동일한 작업을 수행한다.

5글자  이상인 문자열만 빈도수 구하기

=> /input/README.txt파일을 이용

=>output

/mywork/wordcount_exam

 



해쉬맵에 날짜 집어넣고 +1 해서 데이터 집어넣으면 오랜 시간이 걸린다.

hdfs의 /input에 저장하기

/mywork/nasdaq



.csv파일은 String[] temp = value.toString().split(","); 이렇게 써 주어야 한다.-ㅡ

[hadoop@hadoop01 ~]$ /home/hadoop/hadoop-1.2.1/bin/hadoop fs -put /home/hadoop/hadoop-1.2.1/1987.csv /input_data
[hadoop@hadoop01 ~]$ /home/hadoop/hadoop-1.2.1/bin/hadoop fs -ls /
bin/   boot/  dev/   etc/   home/  lib/   lib64/ media/ mnt/   opt/   proc/  root/  run/   sbin/  srv/   sys/   tmp/   usr/   var/
[hadoop@hadoop01 ~]$ /home/hadoop/hadoop-1.2.1/bin/hadoop fs -ls /input_data
Found 1 items
-rw-r--r--   3 hadoop supergroup  127162942 2020-02-20 16:47 /input_data/1987.csv



[hadoop@hadoop01 ~]$ /home/hadoop/hadoop-1.2.1/bin/hadoop fs -put /home/hadoop/hadoop-1.2.1/1987.csv /input_data
[hadoop@hadoop01 ~]$ /home/hadoop/hadoop-1.2.1/bin/hadoop fs -ls /
bin/   boot/  dev/   etc/   home/  lib/   lib64/ media/ mnt/   opt/   proc/  root/  run/   sbin/  srv/   sys/   tmp/   usr/   var/
[hadoop@hadoop01 ~]$ /home/hadoop/hadoop-1.2.1/bin/hadoop fs -ls /input_data
Found 1 items
-rw-r--r--   3 hadoop supergroup  127162942 2020-02-20 16:47 /input_data/1987.csv



[hadoop@hadoop01 ~]$ /home/hadoop/hadoop-1.2.1/bin/hadoop jar hadoop-mapred-examples.jar mapred.exam.air.AirDriver /input_data/1987.csv /mywork/air_result_1



#### #{title} 의미 '?' 의미로서 title변수의 값을 넘겨준다는 의미이다.



 

