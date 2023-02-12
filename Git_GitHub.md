# Git과 GitHub

# 오랜만에 해서 까먹어서 다시 정리
-제일 처음에 커밋하기 위해 해야 하는 것
  - 1. git init
  - 2. git add *
  - 3. git commit -m '주석'
- 여기 밑에 3개는 그냥 복붙 하면 됨
  - 1. git remote add origin '깃허브 주소'
  - 2. git branch -m main
  - 3. git push -u origin main 

## 7/4

- 깃 허브에 문서 올리는 법
- git init 깃에 저장
- git status 깃의 상태 목록 확인
- git add tigers.yaml(파일이름) 특정 파일 담기
- git add . 모든 파일 담기

## 7/5

- .gitignore 깃에서 숨기고 싶은 내용(.gitignore 형식 검색해서 사용하기)
- git commit -m" "( " "안의 이름으로 commit)
- git log (commit 한 목록을 볼 수 있음)
- git commit -am " "(add와 commit를 한꺼번에)(새로 추가된 파일(untracted)이 없을 때)

- reset : 원하는 시점으로 돌아간 뒤 이후 내역들을 지웁니다.
- git reset --hard 해쉬번호
- revert : 되돌리기 원하는 시점의 커밋을 거꾸로 실행합니다.(기록을 남겨야 될 때)(특정 영역만 다시 해야 할 때)(협업할 때)
- -revert를 많이 씀
- git revert 해쉬번호
- git revert --no-commit (되돌릴 커밋 해시)

- git switch (새로운 branch를 만들어서 수정하기 쉽게 만들어 놓는 것)

- merge : 두 브랜치를 한 커밋에 이어붙입니다.(복사-붙여넣기) -브랜치 사용내역을 남길 필요가 있을 때 적합한 방식입니다.(commit하나가 더 생성) -다른 형태의 merge에 대해서도 이후 다루게 될 것입니다.
- rebase : 브랜치를 다른 브랜치에 이어붙입니다.(잘라내기-붙여넣기) -한 줄로 깔끔히 정리된 내역을 유지하기 원할 때 적합합니다.(새로 붙이는 branch는 내역이 남지않음) -이미 팀원과 공유된 커밋들에 대해서는 사용하지 않는 것이 좋습니다.
- git switch main
- git merge add-coach
- main에다가 add-coach를 붙임
- git branch -d add-coach(사용 끝난 브랜치 삭제)
- rebase 는 뭔가 반대로 해야됨
  붙이려고 하는 branch(new-teams)로 switch 한 뒤에 main브랜치에 붙이고
- git rebase main: main branch가 new-teams branch 보다 밑에 있으므로 main branch로 이동한 후에 git merge new-teams 를 해야된다.

- merge했을때 오류가 뜨면 merge를 중단 시키는 것 git merge --abort
  rebase 도 똑같이 해결함 git rebase --abort

- 충돌 수정한 뒤 git add .
  하고 git revase --continue 한 뒤에 main에 붙여서 필요없어진 것들을 git branch -d 하면 됨 (강제 삭제 하고 싶을 떄는 git branch -D 이름)

## 7/6

- 깃허브는 깃을 모아 두는 허브
- 예를들어
  - git remote add origin https://github.com/99shin/git-practice.git
  - git branch -M main
  - git push -u origin main
- 깃허브에 설정해둔 깃을 올리는 코드

  - 폴더에 마우스 우클릭 후 git bash here 클릭
  - git clone https://github.com/99shin/git-practice.git 하면 모든 파일과 git 의 관리내역을 복사

- git push 하면 git hub에 수정한거 바로 올라감
- git pull 하면 git hub에서 수정한거 바로 다운 받음

- pull과 push를 동시에 해야되면 git pull --no-rebase

- #cmd 에서 git하기 위한 용어들과 기본 설정
  - c드라이브 가는법 cd\
  - workspace 파일 만드는 법: mkdir workspace
  - workspacd 폴더 안으로 들어 가는법 cd workspace(이 상태에서 하는 작업은 -로 표시해놓음)
    - -그 뒤에 mkdir git_test라고 하면 git_test라는 폴더가 workspace안에 생성됨
  - -git init를 하면 숨겨진 .git파일이 생성됨(이건 변경사항이 저장되는 파일) -상태를 알기 위해선 git status
  - -git add 뒤에 파일명과 확장자를 적으면 git status 할 시 변화를 관찰할 대상으로 나옴
  - -commit할려면 git commit 뒤에 파일명과 확장자 -m" " 할 시 변화 이력을 저장함
  - -git ignore 할려면 .gitignore라는 파일을 만든 뒤에 안에다가 무시할 파일을 적어둠, 그 후에 cmd에서 mv .gitignore.txt .gitignore로 하면 .gitignore를 .gitignore.txt로 생각할 수 있음 (그렇게 하면 파일 명이 사라져 보일거임)(mv가 안되면 move) -그 뒤에 무시할 이름으로 만든 파일을 생성하고 git status하면 무시할 파일이 안나옴
  - -commit 된 디렉토리에서 파일을 지우고 싶을 때는 git rm 파일이름.확장자
  - -git log 하면 log를 볼 수 있음(해시코드, 작성자, 날짜, commit 내용)
  - -git log에 나온 해시를 사용하면 그 상태로 되돌릴 수 있음 git checkout 해쉬번호

## 7/7

- branch를 만들고 싶으면 git branch 이름
- 해당 branch로 바꾸고 싶으면 git checkout 이름
- 현재 브랜치를 확인하고 싶으면 git branch
- git remote는 remote 저장소 확인
- git remote -v remote 주소
- git remote add 이름
- git remote rm 이름
- 순서는 git add remote 이름
- git commit remote
- git push origin master
- 용어
  - clone
    - clone을 하고 싶을 때는 github의 주소를 복사 한 뒤에 clone하고 싶은 파일을 가서 마우스 우클릭 후 git bash here을 한 뒤에 git clone 해당주소
  - pull
  - fetch
- Fork&Pull Request(PR)
  - Fork 남의 github repository를 내 것으로 가져오는 것
  - PR Fork로 가져온 남의 코드를 수정후 가져가 달라고 요청하는 것(내가 만든거 들고가서 넣어주세요)
- stash
  - stash 는 일종의 임시저장소(후입선출)
  - 사용은 git stash
  - git stash list 하면 stash 목록 확인
  - git stash apply 하면 가장 최근의 stash들고옴
  - git stash drop 하면 가장 최근의 stash 삭제
- head와 tag
  - head는 내가 현재 commit한 가장 최신의 상태
  - tag는 branch 한 내용중에서 특정 부분을 북마킹 해놓은 거(빠르게 찾기위해서 작성자가 원하는 위치에 해놓은 것)
