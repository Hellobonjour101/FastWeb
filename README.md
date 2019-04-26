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
  :wq
  
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
```
Hyosuns-MacBook-Pro:gitfth hyosunkim$ git config --global user.name HSkim
Hyosuns-MacBook-Pro:gitfth hyosunkim$ git config --global user.email hskim@gmail.com
```
git config --global user.name: 해당 파일에 제작자의 이름을 세기는 일<br>
git config --global user.email: 해당 파일에 제작자의 이메일을 세기는 일<br>
--> 딱 한번만 하면 된다.<br><br>

```
Hyosuns-MacBook-Pro:gitfth hyosunkim$ git commit
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch master
#
# Initial commit
#
# Changes to be committed:
#       new file:   f1.text
#
~
~
~
~
```
git commit: commit 명령어<br>

```
version 1.
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch master
#
# Initial commit
#
# Changes to be committed:
#       new file:   f1.text 
~
~
~
~
: wq


Hyosuns-MacBook-Pro:gitfth hyosunkim$ git commit
[master (root-commit) f35bd67] version 1
 1 file changed, 2 insertions(+)
 create mode 100644 f1.text
  ```
***[i]*** : 키보드 i버튼을 눌러서 INSERT가 가능하게 만들자 <br>
맨윗줄에 commit이 변경된 사항을 적고 (ex.version 1) <br>
***[:]*** : 키보드 :버튼을 눌러서 명령어를 쓸수 있도록 한다 <br>
wq : write quite 저장하고 끝낸다는 명령어 <br>

```
Hyosuns-MacBook-Pro:gitfth hyosunkim$ git log
commit f35bd678a2c5d3da1748b310bd57251c18445050 (HEAD -> master)
Author: HSkim <hskim@gmail.com>
Date:   Fri Apr 26 18:50:16 2019 +0900

    version 1
```
git log: 히스토리가 보인다. (ex. 내가 맨 윗줄에 적은 version 1 이라고 적은 내용과 작성자의 이름, 이메일, 작성날짜가 보인다)<br>

```
Hyosuns-MacBook-Pro:gitfth hyosunkim$ vim f1.text
 source code:1
 source code:2
 ~
 ~
 ~
 ~
 ~
 ~
 :wq
 
 Hyosuns-MacBook-Pro:gitfth hyosunkim$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   f1.text

no changes added to commit (use "git add" and/or "git commit -a")
```
vim f1.text <br>
[i] - 새로운 수정사항(source code:2)을 입력 - [esc] - :wq <br>
git status: fi.text가 modified되었다는 사실을 알 수 있다.  <br>

```
Hyosuns-MacBook-Pro:gitfth hyosunkim$ git add f1.text

Hyosuns-MacBook-Pro:gitfth hyosunkim$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	modified:   f1.text


Hyosuns-MacBook-Pro:gitfth hyosunkim$ git commit
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch master
# Changes to be committed:
#       modified:   f1.text
#                                                                                                       
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               

```
git add f1.text <br>
git status <br>
[i] - 새로운 수정사항(version 2.)을 입력 -[esc] - :wq

```
Hyosuns-MacBook-Pro:gitfth hyosunkim$ git log
commit 80e013dfeba6f1e8dc81da7208fc91e83fb7764a (HEAD -> master)
Author: HSkim <hskim@gmail.com>
Date:   Fri Apr 26 19:05:18 2019 +0900

    version 2

commit f35bd678a2c5d3da1748b310bd57251c18445050
Author: HSkim <hskim@gmail.com>
Date:   Fri Apr 26 18:50:16 2019 +0900

    version 1
```

## add(commit 대기상태 = stage area) - commit
***git은 commit 전에 add를 꼭해야 합니다. ***
```
Hyosuns-MacBook-Pro:gitfth hyosunkim$ cp f1.text f2.text

Hyosuns-MacBook-Pro:gitfth hyosunkim$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	f2.text

nothing added to commit but untracked files present (use "git add" to track)

Hyosuns-MacBook-Pro:gitfth hyosunkim$ git add f2.text

Hyosuns-MacBook-Pro:gitfth hyosunkim$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   f2.text


```
cp: 새로운 파일이 복사(copy)되는 명령어 <br>
cp - git status - git add - git status - git commit <br>

```
version 3
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch master
# Changes to be committed:
#       new file:   f2.text
#
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
~                                                                               
:wq
```
[i] - 새로운 수정사항(version 2.)을 입력 -[esc] - :wq <br>

```
Hyosuns-MacBook-Pro:gitfth hyosunkim$ vim f1.text
Hyosuns-MacBook-Pro:gitfth hyosunkim$ vim f2.text
```
각자의 파일에 수정사항을 입력하고, f1.text만 [git add]를 한다면<br>
[git commit]을 했을때 f2.text는 변경사항이 저장되지 않는다. ***(선택적 commit)*** <br>
