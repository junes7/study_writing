# Django Intro

## Start Django

1. 장고 설치

```bash
pip install django==2.1.15
pip list
```

2. 프로젝트 생성

```bash
django-admin startproject <프로젝트 명>
```

장고 서버를 아래의 명령어로 실행해준다.

```bash
python manage.py runserver
```

그 다음 127.0.0.1:8000으로 접속하면 다음과 같은 화면이 나온다.

![image-20200609163244597](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200609163244597.png)



3. 프로젝트 생성 시 제공되는 파일

* manage.py
  * 전체 Django와 관련된 모든 명령어를 manage.py를 통해 실행 합니다.

* `__init__.py`
  * 현재 `__init__.py`파일이 존재하는 폴더를 하나의 프로젝트, 혹은 패키지로 인식하게 해주는 파일 

* settings.py
  * 현재 프로젝트의 전체적인 설정 및 관리를 위해 존재하는 파일
* urls.py
  * 우리 웹 서비스로 접근하기 위한 경로가 있는 파일
  * 내 프로젝트에 접근할 수 있는 경로를 설정하기 위한 파일
* wsgi.py
  * 설정한 것을 배포해주는 역할을 해준다.

아래와 같이 사용할 앱을 생성을 해주고 settings.py 가서 등록을 해준다.

![image-20200609164934989](images/image-20200609164934989.png)

settings.py 에서 설정해 주어야 하는 요소

![image-20200609165128803](images/image-20200609165128803.png)

위와 같이 'pages'앱을 추가 해주고 밑과 같이 장소와 시간 설정도 변경해준다.

![image-20200609163546003](images/image-20200609163546003.png)









