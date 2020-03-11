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



classNotFoundException 에러가 뜨면 jar파일을 export해서 추가해 주어야 한다.

그리고 수정사항이 생기면 생길때마다 jar파일 생성해 export해서 추가해 주어야 한다.



















