# stash

## 기본 명령어

```bash
#1. stash 공간에 작업내역 저장
$ git stash

#2. stash list 보기
$ git stash list 
#3.

$ git pull
```



*  로컬에서 작업하고 있던 중, pull을 받아서 원격 저장소에 새로운 내용을 반영 해야 하는 경우

```bash
$ git pull origin master


#1. 커밋허거나 => 버전으로 남겨도 되는 경우
#2. stash => 작업 중일 때





```

* 해결 방법

```bash
$ git stash
$ git pull origin master



#만약 동일 파일 수정이 있으면, conflict를 발생시킨다.
$ git stash pop


```

