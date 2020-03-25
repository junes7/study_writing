# Android

## Android 설치방법

![image-20200323091918391](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200323091918391.png)



![image-20200323092151624](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200323092151624.png)





AVD 안드로이드 버추얼 디바이스 -JVM과 같은 의미

![image-20200324102455055](images/image-20200324102455055.png)

위와 같이 선택해주고 폴더는 동일하게 설정해주고 설치해준다.





![image-20200324102610166](images/image-20200324102610166.png)

설치가 끝났을 때 Start Android Studio  체크 해제하고 Finish 눌러서 닫아준다.. 

그리고 윈도우에서 Android Studio Setup Wizard 실행해준다.



![image-20200324102728912](images/image-20200324102728912.png)

위처럼 Do not import settings 체크하고 설정을 계속해준다.



![image-20200324102803175](images/image-20200324102803175.png)



위에서 standard 타입을 선택해준다.

![image-20200324102821635](images/image-20200324102821635.png)



테마는 기호에 맞게 설정해준다.





![image-20200324103128622](images/image-20200324103128622.png)

그리고 위 페이지에서 설정을 기다려준다.

![image-20200324104613619](images/image-20200324104613619.png)

그리고 설치가 위와 같이 끝나면 

![image-20200324104638015](images/image-20200324104638015.png)

이 페이지에서 start a new Android Studio project를 선택한다.











## 컴포넌트 기반

라이프 사이클을 안드로이드 내부에서 관리한다.

##### Activity - 화면을 의미

##### Service - 화면이 아닌 back단에서 실행되는 것. 눈에 보이지 않지만 서비스가 뒤에서 실행되고 있다.

##### Content Provider -  어플리케이션 내에서 사용할 수 있는 데이터를 '공유'하기 위한 컴포넌트이며 '어플리케이션 계층'과 '데이터 계층'을 분리하여 중간 가교 역할을 한다.

##### BroadcastReceiver - phone의 상태를 알려주는 역할을 한다. 

##### Intent -하나의 컴포넌트에서 다른 컴포넌트들을 실행시킬 수 있는 객체  





## 리소스의 의무화

리소스의 R

​	문자열 이미지

​	화면 

​	외부파일 R.java







![image-20200324105049740](images/image-20200324105049740.png)



여기 위에서 wear OS 는 시계와 지도 mark 위젯을 의미하고 phone and tablet은 스마트폰이나 tablet pc기본설정, TV는 티브이, Automotive는 자동차, Android Things는 사물인터넷(IoT)을 의미한다. 



package name은 사람들이 앱 마켓에 올라갔을 때 인식하는 코드명으로 쓰일 것이기에 식별할  수 있게 유일한 키로 설정해줄것



![image-20200324105340355](images/image-20200324105340355.png)



위의 phone and tablet 에서 empty activity를 선택하고 save location에서 폴더를 선택하고 select path에서 5번째 버튼을 누르고 새로운 폴더를 만든다. 

![image-20200324105742706](images/image-20200324105742706.png)

언어는 java이고 minimum SDK는 Android 4.1 버전을 선택한다.

위에서 help me choose를 누르면 아래와 같이 나온다. 여기서 보면 4.1 Jelly Bean 버전은 99.6%의 사용자가 사용하고 있다는 의미이다.

![image-20200324105603583](images/image-20200324105603583.png)



![image-20200324105854811](images/image-20200324105854811.png)

위와 같이 프로젝트 설정을 하고 finish(마침) 버튼을 누르면 위의 화면처럼 나온다.

File → settings

![image-20200324111550230](images/image-20200324111550230.png)





![image-20200324111610448](images/image-20200324111610448.png)





![image-20200324111819575ㅅ](images/image-20200324111819575.png)

상위 오른쪽 AVDM버튼을 클릭해서 Android Virtual Device Manager 를 열고 여기서 create virtual device configuration 열어서 Nexus 5X를 선택하고 next버튼을 눌러준다.

![image-20200324112029669](images/image-20200324112029669.png)

그러면 위와 같은 페이지가 뜨는데 여기서  Q다운로드 선택하고 아래와 같이 SDK Quickfix Installlation에서 accept 선택하고next버튼을 눌러서 설치를 해준다. (Q for Android 10 version)   

![image-20200324112048806](images/image-20200324112048806.png)





![image-20200324112410736](images/image-20200324112410736.png)

그리고 설치가 다 되면 위 화면에서  finish 버튼을 눌러 설치를 완료해준다.

![image-20200324112506646](images/image-20200324112506646.png)

그리고 나면 위와 같이 화면이 바뀌어 있다.

![image-20200324114250707](images/image-20200324114250707.png)

설치되고 나면 위 화면에서 finish를 누른다. 그러면 아래와 같은 화면이 나온다.

![image-20200324114354737](images/image-20200324114354737.png)



![image-20200324114456589](images/image-20200324114456589.png)

그리고 위의 빨간 동그라미 실행 버튼을 키면 왼쪽처럼 google 마크가 뜬다.

![image-20200324114559372](images/image-20200324114559372.png)

그리고 실행이 끝나면 왼쪽 처럼 HelloWorld가 뜬다.



![image-20200324131638597](images/image-20200324131638597.png)





![image-20200324131803063](images/image-20200324131803063.png)





![image-20200324132032697](images/image-20200324132032697.png)

안드로이드의 logcat이용해서 기록을 확인한다.

servlet에서 요청이 들어오면 doGet() doPost( )해서 서비스 하는 것처럼 activity 는 만들어지는 시점이 있 ek.



![image-20200324132713897](images/image-20200324132713897.png)

위에서 MainActivity 클래스의 상위 클래스는 AppCompatActivity이고 이 안에 onCreate라는 메소드가 있고 반드시 필요하다.



![image-20200324135032669](images/image-20200324135032669.png)





![image-20200324133430721](images/image-20200324133430721.png)

AndroidManifest는 안드로이드 설명서 파일이다.



MainActivity는 화면을 만드는 부분이다.

이미지 파일이 저장되는 곳이다.





![image-20200324134012384](images/image-20200324134012384.png)

위 빨간줄 쳐 놓은 hdpi 등은 해상도에 따라서 나누어 놓은 것이다.

![image-20200324135208341](images/image-20200324135208341.png)

Mainactivity 폴더는C:\iot\work\androidWork\HelloWorld\app\src\main\java\com\example\helloworld  이 경로에 있다.







![image-20200324134221914](images/image-20200324134221914.png)

앱으로 추출할 때 저 경로에 있는MainActivity 파일들이 실제로 압축된다.









![image-20200324134649214](images/image-20200324134649214.png)

여기서 /를 기준으로 왼쪽은 폴더명 /를 기준으로 오른쪽은 파일명이다.

@은 reference 한다는 의미이다.



![image-20200324142232966](images/image-20200324142232966.png)







![image-20200324142100323](images/image-20200324142100323.png)



![image-20200324142839594](images/image-20200324142839594.png)

설정을 다 했으면 위와 같이 run → run activity를 눌러서 실행해준다.







새로운 프로젝트 작성

new project

App명: firstPro

package: exam.day01.first

프로젝트명: firstPro

화면에 표시된 레이블을 지우고 버튼 세 개를 추가

확인, 취소, 삭제

글꼴 변경

font-family: 

avd에 실행해보기



AndroidManifest.xml 파일에는 한글로주석을 달면 안 된다.

![image-20200324151603806](images/image-20200324151603806.png)

onclick을 눌르려고 해도 아무것도 안 뜬다. 이때 

![image-20200324151906894](images/image-20200324151906894.png)

위와 같이 설정해 주었을때 라이브러리가 추가 안 되어서 빨간색으로 뜬다. 이때 alt shift 엔터를 눌러서 import 해준다.



![image-20200325093158859](images/image-20200325093158859.png)



![image-20200325092927104](images/image-20200325092927104.png)



### View

match-parent의미는 자기가 갖고 있는 폰 사이즈만큼 꽉 차게 layout을 형성하겠다라는 의미이다.

```visual basic
#view_basic_property.xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".MainActivity">
    
    <Button
        android:id="@+id/btnOk"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Button" />

    <Button
        android:id="@+id/btnSearch"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Button" />

    <Button
        android:id="@+id/button3"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Button" />

</LinearLayout>


```

<!--configuration for android-->

layout_width: view의 너비
layout_height: view의 높이
orientation: 배치방향

id:각 위젯을 식별할 수 있는 이름

​	btn

​	txt

margin: 주위여백

padding: 내부 컨텐츠와 border사이의 간격을 결정

layout_weight: 여백을 해당 view의 사이즈로 포함한다

layout_gravity: parent내부에서 view의 정렬

gravity: view내부에서의 정렬이다.(글자의 위치를 정렬할 수 있다)







.xml 파일은 반드시 닫는 태그가 필요하다.

​	![image-20200325101817527](images/image-20200325101817527.png)

위와 같이 에러가 뜨는 이유는 200이란 숫자 뒤에 단위를 붙이지 않았기 때문이다.

![image-20200325102325883](images/image-20200325102325883.png)

그래서 위와 같이 변경해준다.

200dp란 의미는 1인치당 200개의 pixel(점)이 들어간다는 의미이다. 







![image-20200325095001049](images/image-20200325095001049.png)

위 그림의 layout_height를 match_parent에서 wrap_content로 변경해준다.







패키지 변경과 layout 변경할 때

#### .xml 파일 이름 바꾸는 방법

![image-20200325095651423](images/image-20200325095651423.png)

이렇게 경로를 찾아서 들어가면 아래와 같은 화면이 뜬다.

![image-20200325095937217](images/image-20200325095937217.png)]

여기서 Rename 란에 이름을 view_basic_property.xml로 이름을 변경해준다.

![image-20200325095513063](images/image-20200325095513063.png)

여기서 이름을 변경해준 다음 Do Refactor를 눌러 적용해 주어야지 이름이 바뀐다.

![image-20200325095809423](images/image-20200325095809423.png)

Do Refactor를 누르면 위와 같은 화면이 뜨고 빨간 줄 옵션을 적용해준 다음 OK버튼을 누르면 적용이 된다.

![image-20200325100050258](images/image-20200325100050258.png)





![image-20200325102915653](images/image-20200325102915653.png)





![image-20200325102951880](images/image-20200325102951880.png)

밑의 버튼 layout을 만들려면 layout_margin을 20dp로 만들어주고 padding도 20dp로 설정을 해주면 아래와 같은 설정이 나온다.

![image-20200325103007508](images/image-20200325103007508.png)



![image-20200325104539692](images/image-20200325104539692.png)



![image-20200325104456871](images/image-20200325104456871.png)





![image-20200325105359805](images/image-20200325105359805.png)

그리고 색깔을 아래와 같이 설정해주면

![image-20200325105443321](images/image-20200325105443321.png)

위와 같이 색깔이 나온다.

모든 Linearlayout은 layout 안에 중첩해서 사용이 가능하다.

linear_exam03.xml

constraint layout은 relative layout보다 우수하다.

![image-20200325140918016](images/image-20200325140918016.png)

위와같이 왼쪽과 탑을 눌러서 위치를 조정할 수 있다.

만약 위치에 대한 정보가 설정이 안 되어 있으면 에러가 난다.

anker point

![image-20200325142445376](images/image-20200325142445376.png)

위에서 Add Horizontal Guildline

![image-20200325145223205](images/image-20200325145223205.png)

intent배우기 전까지는 MainActivity이다. 핸드폰의 앱을 시작했을 때 나오는 첫화면을 구성하고 있는 파일이 MainActivity이다.

 

세로형과 가로형이 따라 존재한다.

![image-20200325171412148](images/image-20200325171412148.png)

텍스트 뷰를 사용하기 위해서 file→settings들어가서 위와 같이 설정해준다.



![image-20200325172152403](images/image-20200325172152403.png)

TextView 문서이다.



외부에서 textview의 id로 접근해야 되기 때문에 id로 접근하는 것은 필수이다.

@id 내가 아이드를 줄 때

@android 안드로이드에 설정되어 있는 아이디를 참조해서 쓸 때

![image-20200325173558513](images/image-20200325173558513.png)

저 보라색 블럭 설정된 곳에서 ctrl+q를 누르면 다음과 같이 설명이 나온다.

![image-20200325174629943](images/image-20200325174629943.png)

이런 에러가 발생하였을 때에는 뷰부터 설정하고 TextView 클래스에 불러와야 되는데 뷰도 없이 TextView를 불러와서 에러가 났다. 그래서

![image-20200325174840614](images/image-20200325174840614.png)



![image-20200325174901994](images/image-20200325174901994.png)

위와 같이 수정하고 실행하면 위와 같이 안녕이란 글자가 나온다.



