
# 2일차
 ## 1. 타인과 끝말잇기를 해봄

>`$ git clone https://github.com/hyeonaJ/end-to-end.git`

나를 콜라보레이터로 추가해준 타인 저장소를 clone으로 그대로 복사해 가져옴

1. 끝말잇기 내순서 작성 저장 > add > commit > push 보냄

2. >`$ git pull origin master`

    상대편의 끝말잇기 결과 다시 가져와서 동기화

귀여운 하츄핑으로 시작하여 이 과정을 다시 반복하며 끝말잇기를 해보았음

push와 pull은 대척점에 있어 변경된 개별건들을 올리고 받고 하지만, clone은 개별이 아닌 통째로 다 데려옴

---
## 2. `branch`를 만들어봄

>`$ git branch logout`

로그아웃 기능을 구현하는 "logout" 이라는 이름의 branch를 만들어서 별도로 분리 작업 후 master에 merge하여 반영하기 위해 branch 생성

>`$ git branch`

만들어진 branch를 볼 수 있음
```
 * master
   logout
```

>`$ git switch logout`

터미널에서 현재위치 끝부분에 파란색으로 `(master)`라고 표기되었던 것이 `(logout)`이라고 바뀐 것을 볼 수 있고, `$ git branch` 를 다시 해보면 별표(*)가 logout으로 이동해있음

logout branch에서 logout.py 파이썬파일 생성하여 코드작성

(참고로 switch가 아닌 checkout으로 표기/사용하기도 함, 같은 기능이지만 switch가 가장 최근에 사용하는 기능임)

>`$ git push origin logout `

작업한 결과물을 똑같이 add > commit > push 하는데, 이전에는 `master`를 올렸지만, `logout` branch에서 작업을 했으니 `logout`을 올림

github에서 **Pull Requests** 버튼으로 내가 작업한 branch를 적용할건지 (보통은 상급자에게) 코드리뷰요청

>`$ git switch master`

master로 바꿈

>`$ git merge logout`

merge로 합치는데, 별다른 특이사항이 없다면 그냥 처리됨 (Fast-forward라고 적혀있음) 

충돌이 일어나면 `CONFLICT` 라고 표기됨

어떤것을 적용할지 선택지가 나오는 경우도 있는데, 원하는 항목을 골라서 수정해서 적용하면됨


>`$ git branch -d 삭제할branch이름`

merge 완료 후 더이상 필요없는 branch 삭제하기

---
## 3. `fork`로 백일장(삼행시) 참가 해봄 

고기 2인분으로 contributors 기여자가 되었음

1. github에서

타인 저장소 > **Fork**로 내 저장소로 백일장 양식을 포크떠옴 

2. local에서

>` $ git clone https://github.com/hong00009/backiljang.git`

clone 으로 복제해와서 코드를 열심히 수정 > add > commit > push

(이과정에서는 git init 과 remote add url은 필요하지 않음, 왜냐하면 clone 해올때 이미 .git 폴더까지도 가져오기 때문. origin 또한  github주소로 자동 설정되어 clone시 가져오게됨)

3. 다시 github에서

내 저장소의  **Contribute > Open pull reqests**

포크떠온 원주인 저장소에 보냄, 내코드를 받아준다면 내가 기여자가 됨