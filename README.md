# Git tutorial M43B 

------

## Getting Started with git 전에, 마크다운의 기본 작성 요령.

우리는 Git 기초를 배웁니다

마크다운 기본 용도

*

1. dsf
   1. dd
2. dd
   1.
   1.



​```js
console.log('hi')
df
df
​````

​```html
console.log('hi')
df
df
​````

API : Application Programming Interface

## Cloud9

소개

Const 변하지 않는 변수

Jason view 크롬 익스텐션 : 제이슨 파일을 이쁘게 나타내줌

Static 라우팅 : 글자 그대로 라우팅 해주는 것
동적 : 글자 받아서 라우팅

DApp 폴더 안에 token 폴더엔 truffle init
Erc20 폴더 안에는 unbox tutorial token

Truffle unbox
==> truffle suite에 있는 기본 튜토리얼 코인들!

Openzeppelin
보안 높여주는 오픈소스(안정성 업)

Ganache 가나슈
Remix에서 javaScriptVM이다.
로컬의 가상환경이라, 마구 테스트해볼 수 있다.

## Git Tutorial

$ hanyeoulkim:~/workspace $ ls
README.md
$ hanyeoulkim:~/workspace $ ls -la
total 16
drwxrwxr-x  3 ubuntu ubuntu 4096 Nov  2 04:41 ./
drwxr-xr-x 17 ubuntu ubuntu 4096 Nov  2 04:39 ../
drwxr-xr-x  3 ubuntu ubuntu 4096 Nov  2 04:39 .c9/
-rw-rw-r--  1 ubuntu ubuntu  240 Nov  2 04:46 README.md
$ hanyeoulkim:~/workspace $ git init
Initialized empty Git repository in /home/ubuntu/workspace/.git/
$ hanyeoulkim:~/workspace (master) $ la
.c9/  .git/  README.md
$ hanyeoulkim:~/workspace (master) $ git config --global user.name "Han Foreiter Kim"
$ hanyeoulkim:~/workspace (master) $ git config --global user.email "rnltthr06@gmail.com"
$ hanyeoulkim:~/workspace (master) $ which git
/usr/bin/git
$ hanyeoulkim:~/workspace (master) $ 

### Master 떠있으면 깃이 관리하고 있다는 뜻이다.

$ hanyeoulkim:~/workspace (master) $ pwd
/home/ubuntu/workspace
$ hanyeoulkim:~/workspace (master) $ mkdir learn-git
$ hanyeoulkim:~/workspace (master) $ cd learn-git/
$ hanyeoulkim:~/workspace/learn-git (master) $ 

### 옆 탐색기에는 설정된 이름으로 보이지만 실제로는 workspace 경로이다.

### 그러므로 하나 밑에 더 만들어주자.

### 그리고 깃 init 해주면 master 뜬다.

$ hanyeoulkim:~/workspace/learn-git (master) $ touch index.html
$ hanyeoulkim:~/workspace/learn-git (master) $ ls
index.html
$ hanyeoulkim:~/workspace/learn-git (master) $ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

```
    index.html
```

nothing added to commit but untracked files present (use "git add" to track)
$ hanyeoulkim:~/workspace/learn-git (master) $ 

### Index.html. 만들어준다.

### 그리고 git status 해보면 untracked 되어ㅏ있다고 나온다.

$ hanyeoulkim:~/workspace/learn-git (master) $ git add index.html
$ hanyeoulkim:~/workspace/learn-git (master) $ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

```
    new file:   index.html
```

$ hanyeoulkim:~/workspace/learn-git (master) $ 

### 이제, staged 되어있다고 나온다.

# 깃의 스테이지 단계



### 지금은 스테이지드 단계이므로, 깃 커밋을 해주자. -m은 메세지 남기는거다.

$ hanyeoulkim:~/workspace/learn-git (master) $ git commit -m "First Commit"
[master (root-commit) 450534e] First Commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 index.html

$ hanyeoulkim:~/workspace/learn-git (master) $ git status
On branch master
nothing to commit, working tree clean

### 이제 git status 쳐보면 깔끔하게 나온다.

$ hanyeoulkim:~/workspace/learn-git (master) $ git log
commit 450534e8411b3cedfa22e21d3f8bd6f9064a544a (HEAD -> master)
Author: Han Kim <rnltthr06@gmail.com>
Date:   Fri Nov 2 05:22:47 2018 +0000

```
First Commit
```

### Git log 치면 내 글로벌 설정 현황이 나온다.

### 여기서, commit 450534e8411b3cedfa22e21d3f8bd6f9064a544a 

### 이거는 메세지가 동일한 커밋이 있을 수 있기에 각 커밋을 구분할 수 있는 암호화된 버전 식별자이다.

$ hanyeoulkim:~/workspace/learn-git (master) $ touch a b

### A와 b를 만들고 스테터스 치면

$ hanyeoulkim:~/workspace/learn-git (master) $ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

```
    a
    b
```

nothing added to commit but untracked files present (use "git add" to track)

### 언스테이지드 되어있다.

$ hanyeoulkim:~/workspace/learn-git (master) $ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

```
    new file:   a
```

Untracked files:
  (use "git add <file>..." to include in what will be committed)

```
    b
```

### 자, b는 언트랙드 되어있다. 여기서 커밋해보고 스테터스 쳐보면 어떻게 될까?

$ hanyeoulkim:~/workspace/learn-git (master) $ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

```
    b
```

nothing added to commit but untracked files present (use "git add" to track)

### b만 남아있다.

$ hanyeoulkim:~/workspace/learn-git (master) $ git log
commit c148f542a2ea76f7d78f3036f57cd01e2cb92d54 (HEAD -> master)
Author: Han Kim <rnltthr06@gmail.com>
Date:   Fri Nov 2 05:28:20 2018 +0000

```
A만 커밋해보기
```

commit 450534e8411b3cedfa22e21d3f8bd6f9064a544a
Author: Han Kim <rnltthr06@gmail.com>
Date:   Fri Nov 2 05:22:47 2018 +0000

```
First Commit
```

### 자, 이제 b도 애드해서 커밋해주자.

$ hanyeoulkim:~/workspace/learn-git (master) $ git add b
$ hanyeoulkim:~/workspace/learn-git (master) $ git commit -m "B도 커밋해주기"
[master 244653f] B도 커밋해주기
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 b
$ hanyeoulkim:~/workspace/learn-git (master) $ git log
commit 244653f050abd08e2b7c27b2e19db96596a2c3f5 (HEAD -> master)
Author: Han Kim <rnltthr06@gmail.com>
Date:   Fri Nov 2 05:30:29 2018 +0000

```
B도 커밋해주기
```

commit c148f542a2ea76f7d78f3036f57cd01e2cb92d54
Author: Han Kim <rnltthr06@gmail.com>
Date:   Fri Nov 2 05:28:20 2018 +0000

```
A만 커밋해보기
```

commit 450534e8411b3cedfa22e21d3f8bd6f9064a544a
Author: Han Kim <rnltthr06@gmail.com>
Date:   Fri Nov 2 05:22:47 2018 +0000
$ hanyeoulkim:~/workspace/learn-git (master) $ git status
On branch master
nothing to commit, working tree clean

### 아주 깔끔하게 잘 되어있는 것을 볼 수 있다.

### 여기서 잠깐, git과 github은 다른거다. Git은 버전관리 시스템이고, github은 코드의 협업, 공유다.

### 이제, 리모트리포(https://github.com/hanyeoulkim/git-tutorial.git)를 생성하고 c9의 깃 로컬리포와 연결해줘보자.

$ hanyeoulkim:~/workspace/learn-git (master) $ git remote add origin https://github.com/hanyeoulkim/git-tutorial.git

### 이제 푸쉬하면 리모트리포로 간다는 것을 지정해줬다.

### 푸쉬를 해줘보자.

$ hanyeoulkim:~/workspace/learn-git (master) $ git push -u origin master
Username for 'https://github.com': hanyeoulkim
Password for 'https://hanyeoulkim@github.com': 
Counting objects: 7, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (5/5), done.
Writing objects: 100% (7/7), 680 bytes | 680.00 KiB/s, done.
Total 7 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/hanyeoulkim/git-tutorial/pull/new/master
remote: 
To https://github.com/hanyeoulkim/git-tutorial.git

- [new branch]      master -> master
  Branch master set up to track remote branch master from origin.
  $ hanyeoulkim:~/workspace/learn-git (master) $ 

### 푸쉬를 하고, 유저네임-패스워드 입력해준다. 이제 푸쉬가 완료되었다.

# 정리

## Git 오늘의 명령어

| Command      | Description                    | Example |
| ------------ | ------------------------------ | ------- |
| `$ git init` | $ .git 디렉토리 생성 및 초기화 |         |
