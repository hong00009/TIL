`$ git config --global user.name "이름"`

`$ git config --global user.email "이메일"`

이름/이메일 서명 설정하기 (최초 한번만)

`$ git config --list `

설정리스트 보기. 유저네임/이메일 잘 설정되었는지 볼 수 있음

`$ git init`

git 사용하기 위한 기본적인 디렉토리 .git으로 만들어짐 (최초 한번만)

`$ git status`

상태보기 / 빨간색 : 무언가 변경되었으나 아직 처리가 안됨

`$ git add README.md` / 특정파일하나만

`$ git add . ` / 전체

index 등록함 (commit하기위해 staging area로 올리기)

. 점하나는 현재위치한 디렉토리 전체일괄

`$ git commit -m "남길말"`

add 했던 것들을 commit 함

스테이지 찰칵 > .git 

-m "여기에" 수정사항 간단히 메시지로 작성함

`$ git remote add origin https://github.com/hong00009/TIL.git`
 
  원격저장소 연결 (최초 한번만) 원격저장소 주소를 origin 이라는 이름으로 설정

`$ git remote -v`

설정된 원격저장소 확인

`$ git push origin master`

origin으로 설정해놓았던 github 주소에 master 올리기
(master에는 사연이 있어서... 다른사람들은 main이라고 쓰기도함)
처음하면 github 로그인하라는 창이 뜸

`$ git log --oneline`

로그보기 --간략히 / 윗쪽이 최신정보 / --graph는 파일여러개일때 그래프가 그려짐. 지금은 별거없어서 안보임

파일작성 후 저장 > add > commit > push 
저장안됨 ● 아이콘 확인하여 자주 저장하기