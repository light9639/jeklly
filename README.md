# :zap: Jekyll을 이용한 Github 블로그 생성

## 🎊 Github Respository 생성
- Github의 Respository에서 New를 선택해 새로운 Respository를 만듭니다.<br><br>

![img](https://user-images.githubusercontent.com/95972251/193173480-ef7b3b2d-13eb-49b9-8786-61132183c45a.png)
<br><br>
- 생성시 owner이름.github.io로 작성합니다.

## 🚅 Jekyll 설치하기(윈도우)
 1. Jekyll를 설치해 정적 사이트를 만들려고 할 때, 윈도우의 경우 jekyll를 설치하려면 bash나 ruby를 설치해야 합니다.<br>
  ruby 설치 방법은 <a href="https://seong6496.tistory.com/256">링크 참조</a><br>

 2. ruby가 잘 설치되어 있는 상태면 jekyll를 설치할 수 있습니다. cmd 창에서 다음을 코드를 입력합니다.<br>
 
     ```bash
     gem install jekyll bundler
     ```

![img (1)](https://user-images.githubusercontent.com/95972251/193173997-e07bd189-7ca3-4f08-8754-05dbc1147a49.png)

 3. 잘 설치가 되었는지 확인려면 jekyll -v를 쳐봅니다. 버전이 나온다면 설치가 잘 된 것입니다.

![img (4)](https://user-images.githubusercontent.com/95972251/193176395-f5aa484a-74b6-4f48-bfd8-3ea1864cda1c.png)

## :tada: jekyll로 사이트 생성
 1. 혹시 클론한 폴더에 파일이 있다면 모두 삭제하시고 cmd에서 클론한 폴더로 이동합니다. 다음 명령어를 쳐서 사이트를 생성합니다.

    ```bash
    jekyll new ./
    ```

 2. 생성된 후 bundle를 설치합니다. cmd에 다음을 입력합니다.

    ```bash
    bundle install
    ```
  
 3. bundle 설치 후 jkeyll을 로컬서버에 띄우기 위해 다음을 입력합니다.

    ```bash
    bundle exec jekyll serve --trace
    ```
  
 4. 바로 될 수도 있는데 오류가 발생할 수 있습니다. 오류 문구중에 cannot load such file --brick이 나온다면 다음을 입력합니다.

    ```bash
    bundle add webrick
    ```
  
 5. webrick을 추가한 후 다시 서버를 띄웁니다.

    ```bash
    bundle exec jekyll serve --trace
    ```

 6. 잘 되었다면 cmd 창에 Server address가 보일겁니다. Sever address에 적혀있는 IP로 된 url을 브라우저에 복사해 붙여넣습니다. 

![img (2)](https://user-images.githubusercontent.com/95972251/193174416-70d6d20d-81e5-4858-ab46-ae866f41e3c0.png)

 7. 위에 사진처럼 뜬다면 jekyll 설치가 성공한 것입니다.

## 🆙 Github Repository에 올리기
 - 현재 웹페이지는 로컬에 깔아놓은 bundle로 저의 컴퓨터에서만 열 수 있는 상황입니다.<br>
   이 때문에 로컬에 설치한 bundle을 github에 옮겨 저의 Repository가 주소가 되고 웹에서 열 수 있게 하는 작업입니다.<br>
   **git으로 push를 합니다.**

    ```bash
    git add *  #안되면 git add .gitignore 이거나 git add --all 
    git commit -m '커밋메세지'
    git push
    ```

- push가 잘 되었다면 서버주소가 아닌 본인의 Repository로 넣어도 나오는 사이트가 나오는 것을 볼 수 있습니다.
 
![img (3)](https://user-images.githubusercontent.com/95972251/193176129-9c7f23b3-2929-4fd9-a2d7-33a3909eab90.jpg)

## **:paperclip: 출처**
- 출처1 : https://jekyllrb-ko.github.io/docs/
- 출처2 : https://jekyllrb-ko.github.io/docs/installation/windows/
