# TIL
##  VS 코드 주요 단축키
* `Ctrl + K` -> `Ctrl + \` 위/아래 화면 분활
* `Ctrl + \` -> 좌/우 수평 화면 분활
* `Ctrl + J` -> 터미널 실행 / 닫기 
* `Q`or `Ctrl + C` -> 터미널 입력안되는 에러 해결 단축키 
## 작업폴더 설명
* `html_basic/` : html 기초 연습 파일
* `task/` : 과제제출 폴더
* `README.md` : 배운 내용 기록, 어려운 점 및 막힌 점 자유롭게 기록
### 2025/04/04 - HTML 3일차 문서와 레이아웃
* `h1~h6`,`p`, `br`, `strong`, `em`, `del`, `s`, `sup`, `sub`
### 2025/04/07 - HTML 4일차 레이아웃
* `div`, `span`
* 웹/앱 레이아웃 방향과 의미에 따라 2개 이상의 요소를 묶어주는 레이아웃 요소
* `div`는 생성 시 반드시 그룹을 구분할 수 있는 이름을 설정해야 한다. `span`은 선택!
*  이름 작성 시 주의사항 : 반드시 용도에 맞는 의미있는 영단어 사용!
### HTML 구조 공부 순서
1. 클론 코딩 & 클론 디자인 할 사이트 정하기
2. 피그마에서 와이어프레임 만들기 (레이어, 폴더 이름 주의)
3. 피그잼에 일부 화면 넘겨서 태그 계획하기
4. 계획한 태그를 가족관계에 맞게 트리구조 만들기
5. Vs code에서 실제 HTML 작성하기(트리구조 순서에 맞게 바깥쪽 -> 안쪽순서로!)
### 다른 환경에서 git 이어서 작업하기 (집)
* 새폴더 연결하기
* `git clone 저장소 주소 붙여넣기`
* `cd 지정폴더명`
* 자유롭게 수정 후 저장
* `git status` 상태확인
* `git add .` 스테이징 업로드
* `git commit -m '메세지'`
* `git push origin main` 저장소 업로드
### (위 이어서) 다른 환경에서 git 이어서 작업하기(학원)
* `git pull origin main` 메인에 올렸던 작업을 내려받기
### 바로가기 메뉴 만들기
0. (조건) 화면이 수직으로 충분히 이동할 수 있을만큼 스크롤 준비
1. 바로가기 메뉴 a태그 준비하기
2. 바로가기 위치 div id명 준비하기
3. 위 1번 `a`속성 `href` 값으로 `#`먼저 작성 후 2번 이름 작성하기
4. 위 3번 결과 예시) id가 abcd일 경우 `<a href="#abcd">`
### a 태그의 링크 복습
* `<a href="#"></a>` : 임시링크 (연결페이지 제작 전)
* `<a href="#header">` : 바로가기 링크
* `<a href="./basic/index.html">` : 해당 html 로 이동 (상대경로 링크)
* `<a href="./basic/index.html#main"></a>` : 해당 html에서 특정 영역으로 이동(상대경로링크+바로가기링크)
----
##CSS Style Sheet 
* 외부스타일시트 파일 저장은 **styles**폴더에 `파일명.css`저장한다.
* 위 파일 생성 후 CSS연결을 원하는 HTML파일 head위치에 `<link>`태그로 연결한다.
* HTML 작성 후 HTML의 모든 디자인 형태를 초기화 하는 `reset.css` 반드시 연결!
* 웹글꼴(Noto Sans KR, Pretendard 등) 연결 시 HTML 파일에 `<link>` 태그 연결!
### head 태그 내에 들어가는 link 태그 작성 순서
* 1.웹글꼴 연결 주소
* 2.reset.css
* 3.해당 HTML별 디자인.css
### 디자인 CSS 작성 시 작성 순서 및 주의사항
* **부모->자식**순서로 가장 바깥쪽 부모부터 먼저 선택자를 만들고 디자인한다.
* 레이아웃 관련 요소에 `width, height`속성 작성 시 영역 확인을 위한 `background-color`를 꼭 함께 작성해서 정확히 구분한다. 이때 색상은 쉬운 영역 구분을 위한 `aqua, lime, yellow, pink`등의 밝은 색상 위주로 사용한다.
영역 확인과 디자인 작업을 모두 마친 후 위 색상은 제거로 마무리해야한다.
* 실제 디자인에 들어가는 색상은 rgba 또는 헥사코드로 입력하고 테스트용으로 입력하는 임시 색상은 영문명으로 입력해야한다.
### 자주 이용하는 CSS 속성 값과 기본값 ( 뜻 | 기본값 | 사용예시)
* `letter-spacing` 자간설정 | 0  | letter-spacing : -0.02rem;
* `line-height` 행간설정 | 100% | line-height : 1.5;
* `font-size` 폰트 사이즈 | 16px = 1rem | font-size:1.5rem;
* `color`  폰트 컬러  | color: #000; 
* `background-color` 배경색상 | background-color:#000;
* `width` 가로크기  | width:100px;
* `height` 세로크기 | height : 200px;
* `margin`  바깥쪽 여백  |margin-top:50px;
* `border-redius` 모서리 둥글기 | border-redius:50px;
* `font-wight`  폰트 굵기 | 400 | font-weight:800;
* `font-family` 폰트 설정 | font-family:'Noto Sans KR', sans-serif;