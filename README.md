## Install GIT

```
Hyosuns-MacBook-Pro:~ hyosunkim$ cd Documents
Hyosuns-MacBook-Pro:Documents hyosunkim$ pwd
/Users/hyosunkim/Documents

Hyosuns-MacBook-Pro:Documents hyosunkim$ mkdir gitfth
Hyosuns-MacBook-Pro:Documents hyosunkim$ cd gitfth


Hyosuns-MacBook-Pro:gitfth hyosunkim$ ls -al
total 0
drwxr-xr-x  2 hyosunkim  staff   64 Apr 26 18:07 .
drwx------+ 6 hyosunkim  staff  192 Apr 26 18:07 ..


Hyosuns-MacBook-Pro:gitfth hyosunkim$ git init
Initialized empty Git repository in /Users/hyosunkim/Documents/gitfth/.git/


Hyosuns-MacBook-Pro:gitfth hyosunkim$ ls -al
total 0
drwxr-xr-x   3 hyosunkim  staff   96 Apr 26 18:09 .
drwx------+  6 hyosunkim  staff  192 Apr 26 18:07 ..
drwxr-xr-x  10 hyosunkim  staff  320 Apr 26 18:09 .git

```
cd: change directory <br>
pwd: 나의 현재 위치를 보여준다 <br>
mkdir: make directory <br>
ls -al: 내 디렉토리의 상태를 보여준다. <br>
git init: git을 실행하고, .git이라는 파일(버전이 관리되는 파일)이 생성된다. <br>

## Making file
```
Hyosuns-MacBook-Pro:gitfth hyosunkim$  vim f1.text
  ~
  ~
  ~
  ~
  ~
  ~
  ~
  ~
  -INSERT-
  
  source code:1
  ~
  ~
  ~
  ~
  ~
  ~
  :
  
  
    source code:1
  ~
  ~
  ~
  ~
  ~
  ~
  wq
  
```
vim f1.text: fi.text라는 파일을 만들라는 명령어 <br>
***[i]*** : 키보드 i버튼을 눌러서 INSERT가 가능하게 만들자 <br>
***[esc]*** : 타이핑이 되지 않는 상태로 만든다 <br>
***[:]*** : 키보드 :버튼을 눌러서 명령어를 쓸수 있도록 한다 <br>
wq : write quite 저장하고 끝낸다는 명령어 <br>
-->이렇게 하면 source code:1 이라고 쓴 f1.text 파일이 생성된다. <br><br>

```
Hyosuns-MacBook-Pro:gitfth hyosunkim$ cat f1.text
source code : 1
```
cat f1.text: fi.text라는 파일의 내용이 보여진다. <br><br>

```
Hyosuns-MacBook-Pro:gitfth hyosunkim$ git add f1.text

Hyosuns-MacBook-Pro:gitfth hyosunkim$ git status
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   f1.text


```
git add f1.text: f1.text라는 파일의 버전관리를 추적(track)하라는 명령어 <br>
git status: 상태를 보여달라는 명령어(git이 f1.text라는 파일이 new file이라고 인식하기 시작) <br>



## commit
