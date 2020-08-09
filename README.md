# :two_men_holding_hands: 부캠나우 2주차

![나우누리](https://user-images.githubusercontent.com/33643752/89039227-a40de180-d37c-11ea-889d-6ab1dab66a1b.jpg)

## :closed_book: 2주차 요구사항

- ### **게시판 구현**

  - 댓글 기능이 구현된 게시판
  - 다양한 게시판 카테고리 구현 (코딩, 아재개그, 운동, 음악, 역사, 맛집, 음주 등)

- ### **자연어 처리**

  - 기능 A (주) : 욕설 필터링 / 욕설, 비방을 걸러주는 기능
  - 기능 A (부) : 읽음이 / TTS(CSS) 서비스를 통해 게시글 읽어주는 서비스

## 🔧 2주차 진행 상황

- ### 프론트엔드

  #### ◾ API 명세서 작성

  [![https://i.imgur.com/urcYXIV.png](https://camo.githubusercontent.com/e9ea5739d852de48b81eac2244e87cf3e8269fdc/68747470733a2f2f692e696d6775722e636f6d2f757263595849562e706e67)](https://camo.githubusercontent.com/e9ea5739d852de48b81eac2244e87cf3e8269fdc/68747470733a2f2f692e696d6775722e636f6d2f757263595849562e706e67)

  + 각 request 별 api를 명세하여 백엔드에 전달
    + 게시판조회
      + 게시글 추가 및 수정
      + 게시글 삭제
      + 댓글 추가 및 수정
      + 댓글 삭제

  https://docs.google.com/spreadsheets/d/1FHDqBKA63d_qJh1CecOxFgbN_lqygUrGcopDGJ6Cvn8/edit?usp=sharing


  #### ◾ 웹 프레임워크 : React

  ![reactlogo](https://user-images.githubusercontent.com/60503734/89736487-b8e92400-daa4-11ea-9fa1-c16f3fa6b410.png)

  유저 인터페이스를 만드는 데 사용되는 오픈 소스 자바스크립트 라이브러리로 페이스북에서 개발하였습니다. Components 를 이용한 Class 형식의 웹 제작 툴로, 현재 부스트캠프에서 배우는 자바스크립트를 잘 활용 할 수 있을 거라 생각해서 선택하게 되었습니다. 실시간 동기화로 코드를 수정하면 바로 웹 페이지에 적용됩니다.

  #### ◾ 디자인 프레임워크 : Material UI

  <img src="https://cdn.worldvectorlogo.com/logos/material-ui-1.svg" alt="Material-Ui logo vector" style="zoom:15%;" />

  현재 React를 사용할 경우 가장 많이 이용되는 CSS 라이브러리 입니다. React의 장점인 npm install을 통해 쉽게 설치할 수 있으며, 기본적인 템플릿이나 기능을 제공합니다.

  #### ◾ 메인 화면

  [<img src="https://camo.githubusercontent.com/e2889f9a5293cc91ac3c14a6c6247447d88ed201/68747470733a2f2f692e696d6775722e636f6d2f467031725735512e706e67" alt="https://i.imgur.com/Fp1rW5Q.png"  />](https://camo.githubusercontent.com/e2889f9a5293cc91ac3c14a6c6247447d88ed201/68747470733a2f2f692e696d6775722e636f6d2f467031725735512e706e67)

  현재 구현된 기능은 메인 화면, 글쓰기, 게시물 내용입니다. 댓글 기능을 제외하고 나머지에 집중하였습니다. 일단 게시판은 자유게시판 하나만 구현했으며, 글쓰기를 이용해서 새 글을 올릴 수 있습니다.

- ### 백엔드

  #### ◾ 웹 서버 프레임워크 : django

  ![Image for post](https://miro.medium.com/max/1600/1*MrV3XHs6z0pavU9Ci4ENHA.jpeg)

  처음 Node의 Express와 고민을 했지만, 인공지능과 관련된 많은 라이브러리가 Python으로 제공되고 있어 프로젝트의 프레임워크를 python기반인 장고로 정했습니다.

  #### ◾ Django REST Framework (DRF)

  ![post-thumbnail](https://media.vlpt.us/images/lemontech119/post/f4c75e25-e756-4403-a853-dfe007c0a16a/drf.png)

  프론트엔드와 RESTful하게 소통하기 위해 DRF를 적용하였습니다. 

  ### ◾ API

  ![image](https://user-images.githubusercontent.com/53181778/89704984-32ddb800-d994-11ea-982e-59a5897b4ae4.png)

  게시판의 기본적인 동작을 위한 API들을 제공합니다.

  - 게시물 목록
  - 게시물 등록
  - 게시물 삭제
  - 게시물 보기
  - 댓글 목록
  - 댓글 등록
  - 댓글 삭제

- ### 자연어 처리

  - 사용 라이브러리 : https://github.com/teammatmul/project-purifier
  - 라이브러리 사용 관련 이슈 : https://github.com/boostcamp-2020/relay_03/issues/2
  - SUB기능인 TTS까지 처리하기는 시간적으로 제약이 있어, MAIN기능인 비속어 필터링에 집중했다.
  - `serializers.py` 파일의 `isMalicious`함수로 게시글이나 댓글에 비속어가 포함되어있는지 체크한다.

### :triangular_flag_on_post: 프로젝트 참여자

- #### 2주차

  | **J005_강석민** | **J006_강예원** | **J042_김선관** | **J043_김선우** |
  | :-------------: | :-------------: | :-------------: | :-------------: |
  | **J079_박수연** | **J080_박슬우** | **J116_오정석** | **J117_오지현** |
  | **J153_이유택** | **J154_이은솔** | **J192_조정혜** | **J193_조준형** |