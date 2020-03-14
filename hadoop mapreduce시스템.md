# Mapreduce 구조 복습

이번주에 많은 프로그램을 설치하고 할 것이다.

jobclient







![image-20200309095205913](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200309095205913.png)

파일 실행 결과가 몇 개이냐에 따라 part-r-00000이 몇 개 생성된다.

여기서 r의 의미는 reducer라는 의미이다. 

```bash
[hadoop@hadoop01 hadoop-1.2.1]$ ./bin/hadoop fs -put /home/hadoop/19*.csv /air
[hadoop@hadoop01 hadoop-1.2.1]$ ./bin/hadoop fs -put /home/hadoop/20*.csv /air
[hadoop@hadoop01 hadoop-1.2.1]$ ./bin/hadoop fs -put /home/hadoop/1987.csv /air
[hadoop@hadoop01 hadoop-1.2.1]$ ./bin/hadoop fs -rmr /input/1*.csv
Deleted hdfs://192.168.111.132:9000/input/1987.csv
Deleted hdfs://192.168.111.132:9000/input/1988.csv
[hadoop@hadoop01 hadoop-1.2.1]$ ./bin/hadoop fs -rmr /home/hadoop/19*.csv

```



![](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200309105039314.png)



Map은 10개 reduce는 1개라는 의미이다.



### Combiner

* 사용할 데이터의 크기를 줄이는 것





![image-20200309113627919](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200309113627919.png)

이 에러가 발생하는 이유

.class 파일을 .jar 파일로 묶어주지 않았기 때문이다.



hitproduct 사용할 때

SQL> select rownum,ename,sal
  2  from emp
  3  where rownum<=3;

    ROWNUM ENAME                       SAL
---------- -------------------- ----------
```sql
     1 SMITH                       800
     2 ALLEN                      1600
     3 WARD                       1250
```

SQL> select rownum,ename,sal
  2  from emp
  3  where rownum<=3
  4  order by sal desc;

    ROWNUM ENAME                       SAL
---------- -------------------- ----------
```sql
     2 ALLEN                      1600
     3 WARD                       1250
     1 SMITH                       800
```

SQL> select rownum,ename,sal
  2  from(select *
  3  from emp
  4  order by sal desc)
  5  sorttable
  6  where rownum<=3;

    ROWNUM ENAME                       SAL
---------- -------------------- ----------
```sql
     1 KING                       5000
     2 SCOTT                      3000
     3 FORD                       3000
```
바로 위의 것을 사용할 것



Combiner 사용하기 전

![image-20200309132211999](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200309132211999.png)

Combiner 사용한 후

![image-20200309132259228](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200309132259228.png)



키의 개수만큼 reducer가 호출된다.



### RPC(Remote Procedure Call) 개념

상호 미리 정의된 규격을 준수하여 원격에서 동작하고 있는 프로세스에 포함된 함수를 호출 가능하게 하는 프로세스 간 통신 기술이다.

일반적인 프로세스는 자신의 주소공간에서 존재하는 함수를 호출하여 실행가능하지만, RPC를 이용하면 다른 주소공간에서 동작하는 프로세스 함수를 실행할 수 있게 된다.

분산 컴퓨팅 환경에서 프로세스 간 상호 통신 및 컴퓨팅 자원의 효율적인 사용을 위하여 발전된 기술이다.



![image-20200311102600841](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200311102600841.png)

https://leejonggun.tistory.com/9



상품이 몇 번 집계되었는지 보는 것

ID별로 몇 번 클릭되었는지

첫 번째꺼가 상품번호

두 번째꺼가 접속한 ID

세 번째꺼가 그 ID가 클릭한 횟수



어떤것이 첫 번째걸로 묶이는지 본다

![image-20200311105243047](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200311105243047.png)



![image-20200311105401568](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200311105401568.png)

내부에서 키 값이 계속 변하고 있다

보조정렬을 사용해 작업할 것





![image-20200311162528417](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200311162528417.png)

이파일 링크 복사한 다음에 다운로드 할 것

wget 복사한 링크 웹사이트

wget http://archive.apache.org/dist/sqoop/1.4.6/sqoop-1.4.6.bin__hadoop-1.0.0.tar.gz

classNotFoundException 에러가 뜨면 jar파일을 export해서 추가해 주어야 한다.

그리고 수정사항이 생기면 생길때마다 jar파일 생성해 export해서 추가해 주어야 한다.



![image-20200312092825808](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200312092825808.png)





![image-20200312095406003](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200312095406003.png)

이렇게 스쿱 압축파일을 풀어준다.



![image-20200312104321119](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200312104321119.png)

숨김파일 보이기 설정할 것





![image-20200312104537219](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200312104537219.png)

profile은 리눅스 계정으로 접속해 실행하면 보이는 파일이다.





![image-20200312104826884](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200312104826884.png)

위 파일이나

![image-20200312104902787](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200312104902787.png)

아래 파일들은 잘못 수정해주면 커널 실행이 안 된다. 

그러므로 조심해 주어야 한다.

![image-20200312105319898](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200312105319898.png)



![image-20200312110850229](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200312110850229.png)



어디에서든지 사용하려면 라이브러리.jar 파일이 있어야 한다.

![image-20200312113206024](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200312113206024.png)



![image-20200312114254048](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200312114254048.png)





![image-20200312114853714](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200312114853714.png)



이렇게 실행해서 하둡 실행결과를 오라클 테이블에 넣고 오라클에 가서 확인해본다.







```sql
SQL> select * from pro_comment where pro_comment is null;

PRD_NO                                   MEM_ID                                   PR
---------------------------------------- ---------------------------------------- --
PRD000000016                             lee

SQL> delete from pro_comment where pro_comment is null;

1 row deleted.

SQL> commit;

Commit complete.
null 값으로 잘못 등록된 데이터를 이렇게 지워준다.
```



댓글을 직접 달것

2번은 안 해도 된다.

스텝3은 patternTest를 참고할 것



빅데이터 면접질문



페이지뷰 분석

방문자수 분석

순 방문자수 분석

신규 방문자 수

자유 형식으로 어떻게 분석해야 되는지

#### Sqoop을 써서 export 하는 방법 

```sql
SQL> create table wordcount(
  2  word varchar2(30),
  3  hit varchar2(30));

Table created.
```





```bash
sqoop export -connect jdbc:oracle:thin:@70.12.115.59:1521:xe \
> -username shop -password shop \
> -table wordcount -export-dir /wordcount/part-r-00000 \
> -columns "word,hit"
```

이러면 아래와 같은 에러가 발생한다.

![image-20200313095533817](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200313095533817.png)





```bash
sqoop export -connect jdbc:oracle:thin:@70.12.115.59:1521:xe \
-username shop -password shop \
-table wordcount -export-dir /wordcount/part-r-00000 \
-columns "word,hit" -fields-terminated-by \\t

```

그 에러를 해결하기 위해서 위와 같이 -fields-terminated-by \\t 를 추가해준다.

Apache Flume 데이터 수집 프로그램

![image-20200313101251491](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200313101251491.png)

위 그림에서 네모 부분이 Agent이다.

source는 내가 내부에서 담고 있는 부분이다.

일반적인 구성형태이다.



![image-20200313102248304](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200313102248304.png)





spark 공부할 때에는 kafka도 같이 공부해야 한다.



Sink는 output을 담당하는 객체이다.

Hive로 내보낼 수도 있다.

Thrift도 될 수 있고 nosql이다.

ElasticSearchSink는 기업에서 많이 쓰는 객체이다.



FlumeChannel은 전송하기 위하여 쌓아놓았다가 내보낼 때 사용하는 채널이다.

종류로 JDBC, KAFKA 등이 있다.



밖에서는 Documentation만 보도록 한다.

hadoop01, 02에서 Apache Flume를 설치하여 사용한다.



![image-20200313103712345](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200313103712345.png)

이 빨간 줄 버전을 wget으로 다운받는다.





```bash
[hadoop@hadoop01 hadoop-1.2.1]$ wget http://archive.apache.org/dist/flume/1.6.0/apache-flume-1.6.0-bin.tar.gz
--2020-03-13 19:36:42--  http://archive.apache.org/dist/flume/1.6.0/apache-flume-1.6.0-bin.tar.gz
Resolving archive.apache.org (archive.apache.org)... 163.172.17.199
Connecting to archive.apache.org (archive.apache.org)|163.172.17.199|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 52550402 (50M) [application/x-gzip]
Saving to: ‘apache-flume-1.6.0-bin.tar.gz’

100%[==================================================================================================>] 52,550,402  6.66MB/s   in 11s    

2020-03-13 19:36:53 (4.59 MB/s) - ‘apache-flume-1.6.0-bin.tar.gz’ saved [52550402/52550402]

[hadoop@hadoop01 hadoop-1.2.1]$ cd ~
[hadoop@hadoop01 ~]$ pwd
/home/hadoop
[hadoop@hadoop01 ~]$ ls
access_log.txt                 hadoop-1.2.1         hadoop-mapred-examples.jar  sqoop-1.4.6.bin__hadoop-1.0.0         tb_product.java
apache-flume-1.6.0-bin.tar.gz  hadoop-1.2.1.tar.gz  inputdata.txt               sqoop-1.4.6.bin__hadoop-1.0.0.tar.gz  test
carriers.csv                   hadoop-data          multi-hadoop-examples.jar   sqoop_result.java
[hadoop@hadoop01 ~]$ tar -zxvf apache-flume-1.6.0-bin.tar.gz 
```

#### Flume 설정하는 방법

→ 데이터를 추출하기 위해 사용되는 프로그램

시스템로그, 웹 서버의 로그, 클릭로그, 보안로그..비정형데이터를

HDFS에 적재하기 위해 사용하는 프로그램

대규모의 로그데이터가 발생하면 효율적으로 수집하고 저장하기 위해

관리해주는 프로그램이 필요하다/

→flume, chukwa, scribe, fluentd, splunk(보안쪽에서 많이 사용)

※ 빅데이터 프로그램 안에 내장되어 있는 로그 프로그램이 대부분 flume이기에 Apache Flume 프로그램을 사용해본다.

[설정방법]

1. 다운로드
2. .bashrc에다가 설정정보 등록하는 작업을 해 주어야 한다.

flume-env.sh.template이러면 파일을 인식 못한다.

Flume은 자바 베이스이다.

3. flume-env.sh rename하고 정보등록

   -jdk홈디렉토리

   -hadoop홈디렉토리

4. flume 설정 파일에 등록

-flume-conf.properties.template를 rename해서 XXXX.properties

-flume-agent의 source,channel,sink에 대한 정보를 등록해준다.

```bash
[hadoop@hadoop01 ~]$ source .bashrc 
[hadoop@hadoop01 ~]$ cd apache-flume-1.6.0-bin/conf/
[hadoop@hadoop01 conf]$ ls
flume-conf.properties.template  flume-env.ps1.template  flume-env.sh.template  log4j.properties
[hadoop@hadoop01 conf]$ cp flume-env.sh.template flume-env.sh
[hadoop@hadoop01 conf]$ ls
flume-conf.properties.template  flume-env.ps1.template  flume-env.sh  flume-env.sh.template  log4j.properties
[hadoop@hadoop01 conf]$ cp flume-conf.properties.template console.properties


```

3.

![image-20200313111205537](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200313111205537.png)



[Flume의 구성요소]

flume의 실행 중인 프로세스를 agent라 부르며,  source, channel, sink로 구성

1. source

=> 데이터가 유입되는 지정(어떤 방식으로 데이터가 유입되는지 type으로 명시)

agent명.sources.source명.type=값

1) type

​	-netcat: telnet을 통해서 터미널로 들어오는 입력데이터

​				(bind: 접속IP, port:접속할 port)

​	-spoolDir: 특정 폴더에 저장된 파일

​				(spoolDir: 폴더명)

2. channel

=> 데이터를 보관하는 곳(source와 sink사이의 Queue)

3. sink

=> 데이터를 내보내는 곳(어떤 방식으로 내보낼지를 정의한다.)

​	1) type

​		-logger: flume서버 콘솔에 출력이 전달

​		flume을 실행할 때 -Dflume.root.logger=INFO,console을 추가

​	   -file_roll: file을 읽어서 가져오는 경우

​				(directory: 읽어온 파일을 저장할 output폴더를 명시)

consolidation 통합, 정리



[Flume의 실행방법]

```bash
apache-flume-1.6.0-bin]$ ./bin/flume-ng agent 
--conf conf --conf-file ./conf/console.properties 
--name myConsole -Dflume.root.logger=INFO,console

실행명령어: ./bin/flume-ng agent
옵션:
	--conf: 설정파일이 저장된 폴더명(-c)
	설정파일로 무엇을 읽을건지에 대한 옵션이다.
	--conf-file: 설정파일명(-f)
	--name: agent의 이름(-n)
	-Dflume.root.logger=INFO,console:flume의 로그창에 기록

```

source가 telnet으로 입력하는 데이터인 경우



클라이언트 모드에서 

[hadoop@hadoop01 root]$ telnet localhost 44444

접속한 다음에 빠져나올 때

ctrl+ ] 눌러서 관리자모드 telnet>으로가서 'quit'누르면 빠져나온다.

```bash
#/home/hadoop/apache-flume-1.6.0-bin/conf/myfolder.properties
#agent의 source, channel, sink의 name을 정의
myConsole.sources=fileSrc
myConsole.channels=memChannel
myConsole.sinks=fileSink

#channel에 대한 정보를 명시
#for source
myConsole.sources.fileSrc.channels=memChannel
#for sink
myConsole.sinks.fileSink.channel=memChannel

#source에 대한 정보를 명시(어디서데이터를 가져올 것인지 명시한다)
myConsole.sources.fileSrc.type=spoolDir
myConsole.sources.fileSrc.spoolDir=/home/hadoop/input

#sink에 대한 정보
#화면에 출력하겠다는 의미이다.(That means input things display on the screen)
myConsole.sinks.fileSink.type=file_roll
myConsole.sinks.fileSink.sink.directory=/home/hadoop/output

#channel for detail information
myConsole.channels.memChannel.type=memory
myConsole.channels.memChannel.capacity=1000

```





![image-20200313151649955](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200313151649955.png)

input에 이렇게 넣으면

output에 아래와 같이 생긴다.

output에서 계속해서 파일만 생성해줄 뿐이다.



![image-20200314094126358](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200314094126358.png)



alias를 이용해 다르게 나타낼 수 있다.







그대로 보기위해 지정해 주어야 될 게 datastream이다.



쓰레드가 따로따로 도는 것이다.







exec에 관한 것

![image-20200314103454087](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200314103454087.png)



2번 머신에서 WAS를 잡기위해서 tomcat을 다운로드와 설치를 해준다.



tomcat 점유 확인 방법

```bash
[hadoop@hadoop02 apache-tomcat-9.0.31]$ cd bin
[hadoop@hadoop02 bin]$ ls
bootstrap.jar       ciphers.bat                   configtest.bat  digest.sh         setclasspath.sh  startup.sh            tool-wrapper.sh
catalina-tasks.xml  ciphers.sh                    configtest.sh   makebase.bat      shutdown.bat     tomcat-juli.jar       version.bat
catalina.bat        commons-daemon-native.tar.gz  daemon.sh       makebase.sh       shutdown.sh      tomcat-native.tar.gz  version.sh
catalina.sh         commons-daemon.jar            digest.bat      setclasspath.bat  startup.bat      tool-wrapper.bat
[hadoop@hadoop02 bin]$ ./startup.sh 
Using CATALINA_BASE:   /home/hadoop/apache-tomcat-9.0.31
Using CATALINA_HOME:   /home/hadoop/apache-tomcat-9.0.31
Using CATALINA_TMPDIR: /home/hadoop/apache-tomcat-9.0.31/temp
Using JRE_HOME:        /usr/java/jdk1.8.0_231-amd64
Using CLASSPATH:       /home/hadoop/apache-tomcat-9.0.31/bin/bootstrap.jar:/home/hadoop/apache-tomcat-9.0.31/bin/tomcat-juli.jar
Tomcat started.
[hadoop@hadoop02 bin]$ netstat -nap | grep 8080
(Not all processes could be identified, non-owned process info
 will not be shown, you would have to be root to see it all.)
tcp6       0      0 :::8080                 :::*                    LISTEN      74696/java          
[hadoop@hadoop02 bin]$ ./shutdown.sh 
Using CATALINA_BASE:   /home/hadoop/apache-tomcat-9.0.31
Using CATALINA_HOME:   /home/hadoop/apache-tomcat-9.0.31
Using CATALINA_TMPDIR: /home/hadoop/apache-tomcat-9.0.31/temp
Using JRE_HOME:        /usr/java/jdk1.8.0_231-amd64
Using CLASSPATH:       /home/hadoop/apache-tomcat-9.0.31/bin/bootstrap.jar:/home/hadoop/apache-tomcat-9.0.31/bin/tomcat-juli.jar
[hadoop@hadoop02 bin]$ netstat -nap | grep 8080
(Not all processes could be identified, non-owned process info
 will not be shown, you would have to be root to see it all.)
tcp6       0      0 ::1:46060               ::1:8080                TIME_WAIT   -   

```









admin admin 으로 매니저 페이지 접속



![image-20200314114828032](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200314114828032.png)





![image-20200314135140390](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200314135140390.png)

접속하기 위해서 위와 같이 아이피를 변경해준다.

그리고 export -> WAR 파일 들어가서 war파일을 생성해준다.

![image-20200314135330917](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200314135330917.png)

그리고 파일이 생성 되었는지 아래와 같이 확인해준다.

![image-20200314135250160](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200314135250160.png)

그리고 hadoop02머신의 manager 페이지로 가서 WAR 파일을 선택해소 업로드 하고 배치해준다. 그리고 위에서 2번째처럼 /bigdataShop이 잘 들어갔는지 확인해본다.

![image-20200314135517467](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200314135517467.png)



그리고 아래 주소로 접속해 아래와 같이 잘 나오는지 확인해본다.

![image-20200314140221760](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200314140221760.png)





## Agent Type

모든 Type들을 살펴본 것은 아니며 몇 가지 테스트한 Type에 대해서만 기술한다.

### Source Type

* Avro Source: Agent와 Agent를 연결해 주는 Type이다. Agent끼리 연결할 경우에는 Source와 Sink의 Type를 avro로 해주면 된다.
* Exec Source: 파일을 읽을 때 사용하는 Type이

### Sink Type



### Channel Type





./bin/flume-ng agent -c ./conf/ -f ./conf/hdfs2.properties -n myhdfs
오후 미션
1. 3번에 WAS를 구축
2. WAS에 bigdataShop을 배포
3. 3번에 flume을 설치
4. tomcat의 access log를 hdfs에 저장
-avro 통신
-hdfs
/flume/tomcatlog
5.메일로 제출
-3번의 was manager 화면에 배포된 목록 캡쳐
-hdfs에 저장된 access log캡쳐
-각 머신의 flume 설정 파일

./bin/flume-ng agent --conf conf --conf-file ./conf/console.properties --name myConsole -Dflume.root.logger=INFO,console

[테스트]

하둡머신의 flume 실행

WAS머신의 flume 실행

flume_input 폴더에 로그파일 copy







































