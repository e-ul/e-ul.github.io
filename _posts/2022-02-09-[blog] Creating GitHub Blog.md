---
layout: post
title: GitHub 블로그 만들기🪄
subtitle: 블로그 하나 만들기가 뭐 이렇게 힘드냐...
categories: Blog
tags: [Blog, GitHub, Jekyll, Ruby]
published: true

---


🪄 나도 만들었다 GitHub 블로그 ! ! !  
다시 만들 일은... 없을 것 같지만 기록은 해두기로 했다

## 1. GitHub 계정 생성 

개인 블로그용 플랫폼으로 GitHub Pages를 선택했다면, 당연히 GitHub 계정부터 생성해줘야 한다  
[GitHub](https://github.com/) 에 접속하여 화면 오른 쪽 상단의 Sign Up 을 클릭해주면 아래와 같은 페이지가 뜬다

![GitHub SignUp](https://user-images.githubusercontent.com/98747932/153113835-3801bbab-9b37-44e5-a38f-c8002096fd8c.png)

시키는 대로 email, password, 계정이름 입력하면 계정생성은 금방 끝난다  
<span style="color:grey">~~(근데 github 계정 생성 페이지 언제부터 이렇게 예뻐진거지...)~~</span>


## 2. GitHub Pages용 Repository 생성

계정 생성 끝났으면 놀지 말고 바로 Repository 까지는 생성해 줘야 한다.  
한 번 미루면 계속 안하니까....

![Repository 생성](https://user-images.githubusercontent.com/98747932/153114469-4714bc95-be59-4184-a207-73f22437a717.png) 
![](https://user-images.githubusercontent.com/98747932/153114696-5bbfb1da-d557-455f-ab40-d709e9f90ca2.png)

뭐 위 둘 중 하나의 화면 찾아서 초록색 New 버튼 눌러주고 Repository를 생성해 준다.

![](https://user-images.githubusercontent.com/98747932/153114921-6f7fbf8c-42fb-4681-933c-8e748be9ca6f.png)

나는 이미 Repository를 생성했기 때문에 빨간 경고창이 뜨는 것이니...그건 지나가시고....  
Repository Name에는 나의 **_계정명_.github.io** 를 적어주셔야 합니다.  
왜냐면 계정명이 다르면 가끔 연결이 잘 안될때가 있대요..저는 쫄보니까 그냥 시키는대로 합니다

Repository 공개 설정은 **Public**으로 해야한다. Private로 하면 블로그가 보이지를 않아요... 404의 연속  
Private Repository를 GitHub용도로 쓰려면 Pro구독을 해야한다고 하니.... 각자 알아서 하시면 되겠습니다🤑

README.md는 추가하라는 사람도 있고 아닌 사람도 있는데, 나는 어차피 Jekyll Theme 통째로 다운받아서 적용할 것이기때문에 없이 그냥 바로 생성했다.

## 3. GitHub 블로그에 입힐 Jekyll Theme 고르기

나는 사실 Jekyll Theme는 미리 정해뒀다.  
왜냐면 새 맥이 올 때까지 GitHub 계정/Repository만 만들어 두고 clone땡기지 않았기 때문....!  
나는 새 마음 새 뜻으로 시작하는게 좋아서 새 컴퓨터 올 때 까지 존버<span style="color:grey">~~(존중하며 버티기)~~</span>했다.  
그래서 미리 테마들을 둘러보고 후보를 추려 뒀었지... 후후😎

개인적으로 추려둔 후보들은 다음과 같습니다.  
* Yat
* Mediumish
* Chirpy
* Minimal Mistakes

막상 적용하려고 마지막 선택하려니까 귀찮아서 그냥 적어둔 것 중에 맨 위에 적어둔 걸로 바로... 배포했음  
Jekyll Theme 추천이라고 검색하면 수 없이 많이 나오니까... 캡쳐도 귀찮고 하니까 테마 고르기 관련은 여기까지


## 4. Jekyll Theme 받아서 적용하기

나는 사실 GitHub Pages를 시작하겠다고 다짐하면서 Jekyll을 알게되었는데, 이걸 내 블로그에 적용하려면 생각보다 나름 절차가 필요했다.  
그냥 냅다 fork해서... push한다고 되는 일이 아니었음...😞  
이래서 github은 진입장벽이 있다고 하는 거구나....하지만 너무 쉬우면 재미없다  
징징 짜면서 꾸역꾸역해야 돼 인생이 다 그런거야 지치지마

>여기부터는 기억을 더듬어 작성한 것이므로....순서가 다르거나...그냥 틀렸거나....뭔가 빠져있을 수 있습니다  
>그럼 알려주세요... 수정하면 되잖아요? 같이 알아가면 되지...꼽 주기는 하지말자ㅠ나 기죽어...

### 1. 나의 GitHub Pages용 Repository를 내 Local로 clone

GitHub 블로그는 다른 플랫폼 처럼 웹상에서 Post를 작업하는 방식이 아니라, 내가 Post를 작성하고 Git에 올려 다른사람들이 볼 수 있도록 배포하는 방식이라고 할 수 있겠다.  
그래서 일단 내 블로그 소스를 받아서 Local에서 작업하면서 결과물을 확인하고, 결과물이 맘에 든다? 그때 올려.  
물론 난 맘에 안 들어도 일단 올림. 내 맘임.

무튼 그래서 제일 처음 할 일은 **_2.GitHub Pages용 Repository 생성_** 에서 만든 나의 Repository를 내 PC에 clone해 오는 것이다.

이제... git을 사용해야 한다.  
아니 블로그 하는데 git을 사용해야한다는 것 부터가 일단 진입장벽이다..  
내가 개발자 아니었음 여기서 벌써 울면서 이거 안한다고 때려쳤음

![git clone](https://user-images.githubusercontent.com/98747932/153118371-fba4cb29-89ce-4d5f-8512-aae3c19b2718.png)

나는 이미 테마도 적용하고 commit도 해서 뭐가 많지만 아마 새로 생성한 Repository는 텅~텅~ 비었을 것이다.  
하지만 그런게 뭐가 중요하겠어요. 지금부터 할 건데 ! ! !

내 Local에 저 Repository를 받을 위치를 정합니다. 이건 다 본인 마음대로...  
난 개인적으로 따로 만들어둔 workspace Volume에 GitHub Blog 폴더를 만들어뒀고  
여기에다가 clone을 해오기로 했다.

그러면 이제 git clone을 받아야하니... 다들 terminal을 여세요. iTerms쓰는 사람 많다던데 난 그냥 terminal 씀

```
cd /volumes/workspace/GitHub\ Blog
```

이런 식으로 내가 Repository를 받아올 위치로 cd 명령어를 사용해 이동하고  
냅다 clone 받습니다.

```
git clone https://github.com/e-ul/e-ul.github.io.git
```

git clone 뒤에 clone해 올 Repository 주소를 쓰면 되는데 이건 다 하나하나 치려고 하지말구  
위에 캡쳐 보면 알 수 있듯 Code 클릭하면 나오는 저 주소! 저거니까 복사해서 치도록 합시다.  
이런거 오타나면 찾기 어려우니까 easy~~하게 가자고~  

git clone을 하고 나면  
내가 지정했던 폴더<span style="color:grey">(나의 경우는 workspace/GitHub\ Blog 여기)</span> 아래에 _계정명.github.io_ 라는 폴더가 만들어 졌을 것이다

> 아 git 이 없으시다고요....? 거 참 곤란하군  
> 저는 Mac 기준인데 Mac이라면 일단 HomeBrew를 설치하고...거기서 git을 다운받는 방법을 추천합니다  
> 어차피 HomeBrew는 두루두루 쓸거니까 설치하는게 좋고 제일 쉽다고 생각함  
> 나중에 시간 많고 안귀찮으면........뭐,, git 공부도 차차 해볼게요..나도 잘모르니까 공부해서 써야됨..😖

### 2. 골라 둔 Jekyll Theme 다운받기
![Yat](https://user-images.githubusercontent.com/98747932/153117326-3f3c30ad-8fa1-4dff-b56f-8a269596c007.png)

이것이 내가 선택한 Yat Theme다.   
초록색 Code 버튼을 누르고 download ZIP으로 통째로 내려받아서 나의 Local Git 위치에 풀었다...!

나는 성격이 급해가지고 일단 이게 잘 받아진건지... 작동이 되는지 알아보고 싶은 사람이기때문에 당장에 띄워보기부터 하고 싶었다.  
(push 바로 해서 올리면 웹으로 확인할 수 있지만.... 전 commit이력을 그렇게 허비하고 싶지 않았어요)  
하지만!! gitHub 블로그는? 진입장벽이 높다 그랬다.  
냅다 켜는 법을 모름... 이것도 배워야 돼....  
<span style="color:grey">~~내 블로그 가지기전에 서러워서 울겠어😭~~</span>

Jekyll은 Ruby로 만든 것이기 때문에 Ruby부터 설치해야 한다.

_**Mac 기준**_

Mac 유저라면 꼬옥... HomeBrew 설치해주었으면....너무 편함  
그래서 여러분 모두 HomeBrew 설치했을거라 믿고 진도 나간다 정신차려~

#### Ruby 설치하기

mac의 경우는 ruby가 내장 되어있기때문에 Ruby를 따로 설치해주지 않고 진행하면 권한 문제가 발생한다.  
Ruby 설치 안 해 뒀으면 어차피 이거 뛰어넘고 해도 다시 돌아오게 되어있다 이 말씀~.~

```
brew update  // 일단 Brew 최신버전 맞춰주고
brew install rbenv ruby-build // ruby 설치

rbenv versions // 내가 설치한 ruby 버전 확인
// 여기서 mac은 내장 ruby (System이라고 표시됨)를 사용할 수 도 있다..

rbenv install -l // 설치가능한 ruby list 보기

// 개인적으로 젤 마지막으로 나온 것의 전 거 받는 걸 좋아하기때문에 나는 3.0.3 버전 선택

rbenv install 3.0.3

rbenv versions // 내가 설치한 ruby 버전 다시 확인
// 그러면 아마 새로 설치한 3.0.3과 system이 둘다 보일 것
// 하지만 *로 선택된게 system이라면 내가 새로 설치한 ruby를 선택하도록 해주어야함

rbenv global 3.0.3 

rbenv versions // 내가 설치한 ruby 버전으로 선택되었는지 마지막 확인
```

#### Jekyll 실행해 보기 ~~(실패해보기)~~

```
bundle exec jekyll serve // 이게 jekyll을 local에서 실행해보는 명령임
// 어 안 되네 jekyll bundler 깔아야한대요

gem install jekyll bundler // jekyll bundler를 설치하라기에 함
// 근데 안 됨... 뭔가 환경변수를 설정해줘야 한대요.
```

bundle exec jekyll serve 를 이용해서 실행했을 때 오류없이 잘 떴다면
http://localhost:4000/ 로 접속했을 때 테마를 적용한 내 블로그가 잘 보여야 함.

하지만 난 잘 안...되었음.... 당연함. 방금 받은 뜨끈한 새 Mac임. 설정해둔 게 하나도 없음.  
그래서 앞에서 ruby를 깔았으면 rbenv PATH를 환경변수에 추가해줬어야하는데 그걸 안 했으니 당연히 오류나지~~  
환경변수 설정합니다.

```
cd ~ // home으로 이동하고

ls -al // 뭐있는지 한 번 본다

vim ~/.zshrc
```


Mac은 기본설정이 zsh입니다. bash shell을 사용하는 사람은 .bash_profile을 만드세요

.zshrc 파일에 다음과 같이 입력하고 저장

```
[[ -d ~/.rbenv  ]] && \
  export PATH=${HOME}/.rbenv/bin:${PATH} && \
  eval "$(rbenv init -)"
```

그 다음엔 저장한 환경변수를 적용해주어야하니 까먹지말고 아래 명령어 실행  
bash Shell 사용하시면 .zshrc 자리에 .bash_profile 적어야하는건 다들 눈치깠겠죠

```
source ~/.zshrc
```

그럼 다시 bundler 설치합니다

#### Jekyll 실행해 보기 ~~(또 실패해보기)~~

아까 실패 버전에서는 jekyll bundler를 설치하려고 햇는데 그냥 설치하는 김에 통째로 설치합니다

```
gem install bundler

jekyll -v // jekyll version 확인
//뭔가 이상한거 같다? 싶으면 그냥

gem install jekyll bundler // jekyll bundler 따로도 설치해보고...

cd /volumes/workspace/GitHub\ Blog/e-ul.github.io // 다시 소스있는 폴더로 돌아와서~

bundle exec jekyll serve // 실행!!!
```

하지만 또 안 되었습니다.  
왜냐... webrick 때문임  
[Jekyll Docs](https://jekyllrb.com/docs/) 의 QuickStart를 보니 Ruby 3 이상 버전에서 발생하는 현상이라함.  
뭐든 공식문서 읽어가면서 하자^~^

![add webrick](https://user-images.githubusercontent.com/98747932/153124019-796f1481-b73f-4252-88e0-1e0f91eba34d.png)

```
bundle add webrick
```

#### Jekyll 실행해보기

제가 자꾸 실패해봐서 지치셨나요? 그럴수도 있죠  
하지만 이번엔 진짜입니다.

```
bundle exec jekyll serve // 실행!!!
```

아마 이번에는 떴을거에요...  
혹시나 잘 안되었다면 댓글⌨️남겨주세요... 함께 고민해보시죠...해결은 장담 못 함..

## 4. 내 Repository에 Push하여 배포

아휴 지친다....블로그 하나 만들기가 이렇게 힘들어서야...블로거 하겠습니까???  
하지만 나는 지치는 법을 모르지.. 끝까지 조지고 쉰다.

저는 현재 모습의 블로그를 만들기 위해서.... 받은 소스를 조금 뒤져서  
config.yml을 수정해서 블로그 이름을 바꾸고,  
타이틀 banner image를 변경하고,<span style="color:grey">(assets/images/banners : Yat 기준..다른 테마는 안받아봐서 모름)</span>  
기존에 예시로 들어있던 post들<span style="color:grey">(_posts 폴더 아래)</span>을 지웠습니다.

일단 이 정도만 하고 local에서 잘 뜨는 걸 확인 한 뒤 first commit을 ... ! !  

```
git init // git initialize
git add . // 현재 폴더내의 모든 변경사항을 add
git commit -m "커밋 메시지" // commit....!!
git push -u origin master // 변경사항들을 내 Repository github서버에 반영해! 올려 ! !
```

자 이렇게까지하면... 드디어 나의 blog가 세상의 빛을 보게 됩니다...🥺✨  
https://본인의계정명.github.io/  
로 들어가서 잘 뜨는 지 확인해보고 함께....감격의 시간...가져보시죠


>다시 한 번 말하지만, 틀린 거 잘못된 거 있으면,, 지적해주세요..고칠게요..  
>하다가 잘 모르겠다 싶은 부분도 알려주세요. 함께 고민해봐요 해결해주겠다는 말은 아님☺️  
>모니터뒤에 사람 있어요. 꼽주지마 상처주지마 나 기죽으니까....