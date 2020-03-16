# MongoDB -> NoSQL

## NoSQL(Not Only SQL)

* 특징
  * Oracle 로 만들때는 schema가 필요하다
  * 그러나 NoSQL은 ''비정형데이터''이기에 schema가 없다
  * jSON
  * join을 할 수가 없다. 하나의 문서 안에 모든 데이터가 다 들어간다.
  * schema가 정해져 있어서 테이블이 늘어나고 조인이 복잡해진다.
  * MEAN 스택 기반이다.
  * 입출력이 빈번한 것들을 작업할때 MEAN스택 기반으로 구현을 해준다.

* 사용목적
  * RasberriPi는 debian 계열이라서 MongoDB 설치하고 센서데이터를 관리할 수 있다.
* 설치방법

![image-20200316093821180](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316093821180.png)

빨간줄 되어있는 링크를 선택해준다.

아래와 같이 3.6.17버전에 windows64버전 선택해주고 package는 MSI 선택해준다.

![image-20200316094758771](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316094758771.png)





그리고 다운받은 파일의 오른쪽을 클릭하고 속성으로 들어가면 아래와 같은 디스크 크기를 가지고 있다.

![image-20200316094215913](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316094215913.png)

complete버전 선택해주고 install MongoDB compass 체크해준 다음 설치해준다.

![image-20200316094138576](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316094138576.png)



* 설정 방법

![image-20200316100818613](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316100818613.png)

위와 같은 순서로 해서 환경변수에 들어가서 (path)경로를 설정해준다.

그 다음에 win + R → cmd로 들어간다.

![image-20200316101348689](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316101348689.png)

이렇게 mongod를 치고 들어가면 에러가 발생한다.

data를 DB 저장할 폴더가 없기 때문이다.

내부에서 발생하는 데이터를 폴더 하나에 저장한다.

그래서 아래와 같이 만들고 명령어 치면 아래와 같이 서버가 대기상태에 들어간다.

![image-20200316101820999](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316101820999.png)

이 상태에서 새로운 명령 프롬프트에서 

![image-20200316102436375](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316102436375.png)

위 그리고 아래와 같이 접속한다.

![image-20200316102822928](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316102822928.png)

그러면 아래와 같이 서버에 뜬다.

또 웹 브라우저에서 http://127.0.0.1:27017/이렇게 접속하면

![image-20200316102935507](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316102935507.png)

이렇게 메시지가 뜨고 아래 conn4처럼 메시지가 뜬다.

![image-20200316102711800](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316102711800.png)

그리고 여러개 사용해서 접속하면 위와같이 메시지가 뜨고 다중 접속이 위와 같이 가능하다.

그리고 웹 사이트 document에서 다음과 같이 접속하는 방법을 살펴볼 수 있다.

![image-20200316103117470](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316103117470.png)



### <<명령어>>

* 현재 만들어진 db 확인하기

show dbs;

* database 생성하기

use mydb;

* db 상태 확인할 때

db.stat()

db.stats()

* db logout할때

db.logout()





### <<용어>>

* collection(table): 테이블

* document(record): 레코드

* field(column): 컬럼

* _id: 기본키

![image-20200316104009097](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316104009097.png)

위와 같이 db 상태를 확인할 수 있다.

![image-20200316104624259](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316104624259.png)

use mydb; => 계정 생성

db.createCollection("test") = create table test ~~

test: 컬렉션명(table명)

show collections; = select * from tab;

1. #### Collection (rdbms에서 테이블)

=> 관계형 DB처럼 schema를 정의하지 않는다.

![image-20200316110654718](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316110654718.png)

1) 종류

- capped collection

:고정 사이즈를 주고 생성하는 컬렉션

미리 지정한 저장공간이 모두 사용이 되면

맨 처음에 저장된 데이터가 삭제되고 공간으로 활용

* non cappped collection

:일반적인 컬렉션

Mongo DB는 기본으로 안 올라가 있다.
그러므로 path를 지정해주어야 한다.

mongod -dbpath C:\iot\bigdata\mongodata
Sharding이란 hadoop 처럼 분산저장이 가능하게 해 주는 역할을 해준다.

2)  collection관리

[생성]

db.createCollection("컬렉션명")  -> 일반 collection

=> 각각의 옵션을 설정해서 작업(json)

![image-20200316111242098](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316111242098.png)



db.createCollection("컬렉션명",{옵션list})

![image-20200316111513169](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316111513169.png)

위와 같이 collection을 생성한 후

![image-20200316111742795](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316111742795.png)

위와 같이 확인 가능하다.

[삭제]

db.collection명.drop()

![image-20200316111904630](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316111904630.png)

테이블 삭제는 위와 같이 사용할 수 있다.

[컬렉션명 변경]

db.컬렉션명.renameCollection("변경할컬렉션명");

![image-20200316112002566](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316112002566.png)

테이블 이름을 바꿀때는 위와 같이 사용할 수 있다.

[실습]

mini 데이터베이스 생성

-use mini

emp (size: 10000, capped 컬렉션)

-db.createCollection("emp"

​	{capped:true, size:10000});

shop(일반컬렉션)

-db.createCollection("shop") 

![image-20200316113858370](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316113858370.png)

생성한 collection이 capped인지 non capped인지 확인할 때

데이터베이스 목록,컬렉션 목록을 캡쳐

show dbs;

show collections;

컬렉션 validate()화면캡쳐

2.mongodb에 insert

![image-20200316114606852](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316114606852.png)



[구문]

db.컬렉션명.insert({데이터...})

db.컬렉션명.insertOne({데이터...})

db.컬렉션명.insertMany({데이터...})

-document(관계형 db에서 레코드 개념)에 대한 정보는 json의 형식으로 작성

-mongodb에서 document를 삽입하면 자동으로 

_id 생성 -기본키 역할

"_id": ObjectId("5e6ee81606be3da41efd0467")

​						----------------------------------------------

현재 timestamp + machine Id + mongodb프로세스id + 순차번호

​																								-------------

​																							추가될 때마다 증가

* 스카마가 있는지 없는지 확인

  ![image-20200316114840439](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316114840439.png)

arguments(매개변수)에 있는 것들은 생략 가능하다. 

#### MongoDB 데이터 자료형

MongoDB는 해당 데이터의 type를 1~255사이의 ID값을 부여하여 정의한다.

다음은 몽고DB에서 지원하고 있는 자료형의 목록이다.

| 형식            | 숫자 | 형식                     | 숫자 |
| --------------- | ---- | ------------------------ | ---- |
| 실수형(Double)  | 1    | 정규표현식               | 11   |
| 문자열(String)  | 2    | 자바스크립트             | 13   |
| 객체            | 3    | 심볼(Symbol)             | 14   |
| 배열            | 4    | 자바스크립트(with scope) | 15   |
| 바이너리 데이터 | 5    | 32비트 정수형            | 16   |
| 객체 ID         | 7    | 타임스템프               | 17   |
| 불린(Boolean)   | 8    | 64비트 정수형            | 18   |
| 날짜(Date)      | 9    | Min키                    | 255  |
| 널(Null)        | 10   | Max키                    | 127  |

#### MongoDB 구조

간단하게 MongoDB 구조를 정리하면 다음과 같다

![image-20200316123431142](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316123431142.png)



그러나 필요할 경우, 도큐먼트 내부에도 복수의 도큐먼트를 포함시킬 수 있어 형식이 매우 자유롭다.





![image-20200316131258498](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316131258498.png)

여기서 위와 같이 삽입을 하고

![image-20200316131349860](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316131349860.png)

위와 같이 확인할 수 있다.

![image-20200316131924924](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316131924924.png)

insert는 아래와 같이 할 수도 있다.

![image-20200316132247476](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316132247476.png)

여러개를 한꺼번에 넣을때 배열로 삽입하면 된다.

![image-20200316132731039](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316132731039.png)

그러면 위와 같이 확인 가능하다.

![image-20200316133124996](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316133124996.png)

위와같이 중복해서 값을 넣으려고 하면 위와 같은 에러가 발생한다.



db.customer.insert({id:"kang",pass:"3456",name:"강감찬",
		info:{city:["seoul","busan","sejong"],
		toeicjumsu:[700,800,650,850,855]
		}
		});

db.customer.insert({id:"jang",pass:"1234",name:"장동건",
		info:{city:["인천","안산","안양"],
		toeicjumsu:[555,780,650,900,855]
		}
		});

db.customer.insert({id:"hong",pass:"2345",name:"홍길동",
		info:{city:["수원","파주","교하"],
		toeicjumsu:[480,540,656,770,820]
		}
		});

db.customer.insert({id:"park",pass:"5678",name:"박서준",
		info:{city:["부산","인천","안양"],
		toeicjumsu:[450,500,558,850,950]
		}
		});

db.customer.insert({id:"ha",pass:"6789",name:"하정우",
		info:{city:["파주","서울","안산"],
		toeicjumsu:[700,800,860,870,890]
		}
		});

3. mongodb에 update

-> document수정

-> 조건을 적용해서 수정하기 위한 코드로 json으로 구현



[update를 위한 명령어]

$set: 해당필드의 값을 변경(업데이트를 하기 위한 명령어)

none cappped collection인 경우 업데이트할 필드가 없는 경우 추가한다.

$inc: 해당필드에 저장된 숫자의 값을 증가

$unset: 원하는 필드를 삭제할 수 있다.

업데이트 옵션:

​		multi => true를 추가하지 않으면 조건에 만족하는

​		document 중 첫 번째 document만 update

[구문]

db.컬렉션명.update({조건필드:값},//sql의 update문 where절

​									{$set:{수정할필드:수정값}});//set절

​									{update와 관련된 옵션: 옵션값});

![image-20200316143842967](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200316143842967.png)



db.collection명.update({조건},{$set:{ }},{옵션});



[실습]

1. id가 kang사람의 dept를 "총무"로 변경

2. dept가 "전산"인 모든 addr을 "안양"으로 변경

3. id가 jang인 document의 bonus를 1000 추가하기

4. dept가 "인사"인 모든 document의 bonus에 2000을 추가하기

1. db.score.update({id:"kang"},{$set:{dept:"총무"}});
2. db.score.update({dept:"전산"},{$set:{addr:"안양"}},{multi:true});
3. db.score.update({id:"jang"},{$inc:{bonus:1000}});
4. db.score.update({dept:"인사"},{$inc:{bonus:2000}},{multi:true});



4. mongodb에서 배열 관리

db.score.update({id:"jang"},

​								{$set:

​									{info:

​											{city:["서울","안양"],

​										 	movie:["겨울왕국2","극한직업","쉬리"]

​											}

​									}

​								})

[배열에서 사용할 수 있는 명령어]

$addToSet: 배열의 요소를 추가

:없는 경우에만 값을 추가, 중복을 체크

 literal을 추가할 때 사용한다.

db.score.update({id:"jang"},

​		{$addToSet:{"info.city":"인천"}}

)

$push

배열의 요소를 추가

:중복을 허용

db.score.update({id:"jang"},

​		{$push:{"info.city":"천안"}}

)

$pop

배열에서 요소를 제거할 때 사용

1이면 마지막 요소를 제거,

-1이면 첫 번째 요소를 제거

db.score.update({id:"jang"},

​		{$pop:{"info.city":1}}

)

db.score.update({id:"jang"},

​		{$pop:{"info.city":-1}}

)

$each: addToSet이나 push에서 사용할 수 있다.

여러 개를 배열에 추가할 때 사용

db.score.update({id:"jang"},

​				{$push:

​						{"info.city":

​							{$each:["천안","가평","군산"]}

​						}

​				}

​	);

$sort: 정렬(1.오름차순 정렬, -1:내림차순 정렬)

db.score.update({id:"jang"},

​				{$push:

​						{"info.city":

​							{$each:["천안","가평","군산"],

​							 $sort:1

​							}

​						}

​				}

​	)



db.score.update({id:"jang"},

​				{$push:

​						{"info.city":

​							{$each:["창원","마산","태백"],

​							 $sort:1

​							}

​						}

​				}

​	)

$pull : 배열에서 조건에 만족하는 요소를 제거(조건을 한 개)

db.score.update({id:"jang"},

​				{$pull:{"info.city":"천안"} }

)

$pullAll : 배열에서 조건에 만족하는 요소를 제거(조건을 여러 개)

db.score.update({id:"jang"},

​				{$pullAll:{"info.city":["가평","군산"]} }

)

**score collection을 이용해서 작업해보세요**

**1. song,jang,hong에 다음과 같은 값을 가질 수 있도록 배열로 필드를 추가하세요**

**song : history (영업1팀, 총무, 기획실)**

**jang: history(전략팀,총무,전산)**

**hong : history(영업1팀, 기획실,전산)**

**2. song의 document history에 자금부를 추가하세요**

**3. jang의 document의 history에 마지막 데이터를 제거하세요**

**4. servlet데이터가 100점인 모든 document에 bonus를 3000을 추가하세요. 기존데이터가 존재하면 증가되도록 구현하세요**

**5. song의 lang.ms에 "visual basic","asp",".net"을 한꺼번에 추가하세요**

1.
db.score.update({id:"song"},
	{$addToSet:
		{"history":

		{$each:["영업1팀","총무","기획실"]}
	
		}
	
	}

);

db.score.update({id:"jang"},
	{$addToSet:
		{"history":

		{$each:["전략팀","총무","전산"]}
	
		}
	
	}

);

db.score.update({id:"hong"},
	{$addToSet:
		{"history":

		{$each:["영업1팀","기획실","전산"]}
	
		}
	
	}

);

2.

db.score.update({id:"song"},
	{\$addToSet:{"history":"자금부"}}
);
3.
db.score.update({id:"jang"},
	{​\$pop:{"history":1}}
);
4.
db.score.update({servlet:100},
	{\$inc:{"bonus":3000}},
	{multi:true});
5.
db.score.update({id:"song"},
	{\$addToSet:
		{"lang.ms":
			{\$each:["visual basic","asp",".net"]}
		}
	}
);



게시물과 댓글을 mongodb에 저장
use mydb;
1. board 컬렉션을 생성
db.createCollection("board");

2. document는 5개 insert

no,id,title,content,count,writedate

db.board.insert({no:001,id:"kang",title:"게시글1",content:"안녕하세요1",count:10,writedate:new Date});
db.board.insert({no:002,id:"jang",title:"게시글2",content:"안녕하세요2",count:20,writedate:new Date});
db.board.insert({no:003,id:"hong",title:"게시글3",content:"안녕하세요3",count:30,writedate:new Date});
db.board.insert({no:004,id:"park",title:"게시글4",content:"안녕하세요4",count:40,writedate:new Date});
db.board.insert({no:005,id:"lee",title:"게시글5",content:"안녕하세요5",count:50,writedate:new Date});


3. 2번째 게시물에는 댓글이 3개 추가되도록

update - 하위object와 배열로 구성

댓글의 필드
content,count1,count2,writedate

=> 코드와 실행결과 캡쳐

db.board.update({id:"jang"},
		{\$addToSet:
			{comment:[
				{content:"내용1",count1:1, count2:2,writedate:new Date}
			]}
		}
	);
db.board.update({id:"jang"},
		{\$push:
			{comment:[
				{content:"내용2",count1:2, count2:0,writedate:new Date}
			]}
		}
	);
db.board.update({id:"jang"},
		{\$push:
			{comment:[
				{content:"내용3",count1:1, count2:3,writedate:new Date}
			]}
		}
	);



