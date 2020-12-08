# Git Setting

## 설치
콘솔에서 이용할 때

1. [Git 다운로드] (https://git-scm.com/)
2. Git Bash 실행
3. Git 설치 확인
```Bash
$ git --version
git version x.xx.x
```

## 초기 설정
설정한 내용은 .gitconfig 파일에 저장 됩니다.

```Bash
$ git config --global user.name 사용자명
$ git config --global user.email 메일 주소
```

명령어로 단축키(alias)를 설정할 수 있습니다.  
아래 명령어는 'checkout'을 'co'로 생략해도 실행할 수 있게 설정해줍니다.
```Bash
$ git config --global alias.co checkout
```

### Windows에서 콘솔(Git Bash)을 사용하는 경우
한국어를 포함한 파일명도 올바르게 표시하려면 아래의 설정을 추가 합니다.
```Bash
$ git config --global core.quotepath off
```

커밋 메시지에서 한국어를 사용하는 경우 외부 데이터를 이용해야 합니다.
```Bash
$ git config --global core.editor "\"[사용할 에디터의 경로]\""
```

## 저장소 만들기
1. 새 폴더 생성
2. init 명령어 사용

```Bash
$ mkdir 폴더명
$ cd 폴더명
$ git init
Initialized empty Git repository in  
/해당경로/새 폴더/.git/
```

## Git의 관리 하에 있는 폴더의 작업트리와 상태를 확인하려면, status 명령어를 사용
```Bash
$ git status
```

## Git staging add
git add 명령어로 디렉토리 내의 모든 파일이 Git으로 관리되도록 추가
```Bash
$ git add git_part02_setting.md
```

## 파일 커밋(Commit) 하기
$ git commit -m "setting"

## .gitignore 만들기
제외할 파일 목록을 지정하는 파일
```Bash
$ echo *.log > .gitignore
```