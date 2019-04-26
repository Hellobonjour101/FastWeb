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
  
  coding!
  ~
  ~
  ~
  ~
  ~
  ~
  :
  
  
    coding!
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
esc : 타이핑이 되지 않는 상태로 만든다 <br>
***[:]*** : 키보드 :버튼을 눌러서 명령어를 쓸수 있도록 한다 <br>
wq : write quite 저장하고 끝낸다는 명령어 <br>
