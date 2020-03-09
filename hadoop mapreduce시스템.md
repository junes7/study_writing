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























