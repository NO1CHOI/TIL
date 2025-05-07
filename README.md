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
## 위치속성 float
* 블록, 인라인 요소를 좌(left), 우(rifht) 사용하는 위치 속성
* 좌/우 배치하고 싶은 요소가 형제이 ㄴ경우 사용
* 형제가 3개 이상인 경우 1 -> 2 옆으로 두고 3을 내리고싶은 경우. 형제 3에게 `clear:both`를 선언하여 이전 형제의 float 정렬 제거
## 오른쪽으로 보내고 싶은 형제 요소가 2개 이상이라면?
* 2개를 묶어서 그룹으로 묶어 처리하고 `float:right`하먼반 작성한다.
* `float:right`는 2번 이상 사용하면 역순이 되므로 **한번만 작성해야한다!!**
### float를 적용하는 형제의 부모의 높이가 max-content(기본값)이라면? 
* `overflow:hidden`을 사용해 높이를 안주고 영역 재인식을 시켜 Float에 의한 오류를 제거해야 한다.
## form 태그 관련 속성 주요 뜻과 사용 용도
* 입력 양식 `input type=` text, password, email, search, number 등..
* 선택 양식 `input type=` checkbox, radio, select, option 등..
* 입력 양식과 선택양식에 따라 같은 스펠링 속성의 뜻이 달라지므로 주의해야 한다!
## 양식에 따라 다른 속성의 뜻
* `value` : 입력양식(사용자가 입력한 값(속성작성 X)), 선택양식(사용자가 선택해서 서버에 전송되는 값)
* `name` : 입력양식(사용자가 선택해서 서버에 전송되는 값(작성C)), 선택양식 (2개이상 (1개도 가능)의 선택양식을 묶어준느 동일 그룹(작성 C))
*  입력양식에서 `value`의 초기값을 작성하는 경우:
## form 속성에 사용자정의값을 이름 작성할 경우
* name, value, id, claa 등 속성의 이름을 작성할 때는 **중복명칭_개별명칭**을 섞어서 작성한다.
* 중복명칭에 주로 사용하는 단어 : `admin, user`
* 개별명칭은 요소의 특징에 따라 달라진다(`male, id, btnm pw` 등)
* 중복명칭 설정 시 작성 방향도 동일하게 해야한다.
* `user_id == user_pw` O
* `user_id == pw_user` X
## 목록양식 select, option (선택 목록이 2개 이상인 경우)
* 기존 목록비교해서 외우기 select(ul), option(li)
* `select`태그는 option을 묶어주는 그룹개념으로 그룹 속성(name)이 함께 적용된다
* `option`태그는 사용자가 실제 선택하는 값이므로 데이터 구분값 속성(value) 작성한다.
* `option`태그 작성 시 value 속성은 필수가 아닌 사용자가 선택하는 데이터에만 사용한다.
* 선택 option -> 1,컬러(x) 2, 블랙(black) 3, 화이트(white) 4,코랄(coral) 
## 선택양식 radio, checked 주의사항과 label 주의사항
* radio, checkbox는 name(동일 그룹), value(개별 데이터값)속성을 구붛내서 사용한다.
* `id` 속성을 적용할때는 javascript와 연결을 위해서 하거나 또는 label의 `for` 속성 연결을 위해서 사용한다. 이때 id값은 기존 개별 데이터값을 가진 `value`와 동일한 값을 작성해도 된다
* `label`은 사용자가 선택하는 이미지 또는 글자를 묶어서 작성하고 기존 선택양식 input의 형체로 작성한다면 반드시 `for` 속성을 입력해서 input의 id와 동일하게 입력하고, 반대로 input의 부모로 작성한다면 for을 입력하지 않아도 된다. 대신 이 경우에는 선택하는 이미지 똔느 글자를 반드시 다른 인라인 태그로 묶어야한다.
* input, radio, checkbox는 사용자커스텀 css 디자인이 불가능하기 때문에 사이트에 어울리는 모습으로 디자인하고 싶다면 `display:noen;` 숨기고 선택글자를 묶은 태그에 `background-image`로 디자인해야한다
## input과 label이 형제인 경우 
*  `<input id="a"><label for="a">선택글자</label>`
## input과 label이 부모-자식이 ㄴ경우 
*  `<label><input id="a'><span>선택글자<span></label>`
## button 속성 종류와 사용처
* `button type="속성종류" id="버튼구분명"> 보이는 글자 or 이미지 </button>`
* 속성종류 1. button
* 속성종류 2. submit
## CSS Calc() 함수
* css에서 길이, 비율, 수치 등을 게산할 때 사용하는 함수
* 단위가 다른(px, % 등)값도 계산할 수 있어서 레이아웃 조정 시 유리함.
* `+, -, *, /`산술 연산자 모두 사용 가능
## CSS Calc() 함수 예시
* `height:calc(50vh - 100px);`
* `padding:calc(100% - (10px * 3));` 우선순위 괄호 추가 사용 가능!
* `width:calc(90% - (60px - 5px));` 우선순위도 연산자 앞뒤 공백 필수!
* `width:calc(90% - 65px);`
## Flex layout
* flex는 수평, 수직 1차원 레이아웃으로 메인축과 교차축을 고려하여 다양한 레이아웃을 만들 수 있는 css3의 새로운 레이아웃속성입니다.
* container(부모속성), item(자식속성)에 주는 속성이 다르기 때문에 주의해서 작성해야한다!**기본 시작은 부모**
* `display:flex` 부모(container)대상에 display 명령어로 해당 레이아웃이 flex라는 선언부터 시작합니다.
* 위 flex 선언을 진행 시 메인축은 기본값 수평, 교차축은 기본값 수직으로 정렬됩니다.
## position
## 필수속성 relative, absolute, fixed, sticky
## 선택속성 top, bottom, right, left
* `flex, float`등 포함 위치가 잡혀있는 요소에서 상/하/좌/우로 살짝 이동을 할때는 `position:relative;`
* 형제 요소 또는 부모-자식 요소 관계에서 부모 위치를 기준으로 요소를 겹치거나 현재 위치와는 관계없이 멀리 이동할 경우는 `position:absolute;`
* **주의사항** `absolute` 사용 시 부모들 중 별도의 position 속성이 없다면 `body`를 기준으로 위치가 설정되니 부모 중 원하는 기준 대상에 반드시 position 속서을 함께 작성해야 한다. `absolute, relative, fixed, sticky` 모두 가능! (상황에 따라 조합하기.)
## transition
* `transition:애니메이션적용속성 지속시간 가속도 딜레이속성`
* `transition:속성, 속성, 속성`**2개 이상 속성 작성 가능**
* transition 속성은 hover 등 동작을 따라가는게 아닌 변화하는 css 값이 어떤 요소에 들어가느냐를 기죽으로 적용된다.
### 가속도 종류
* `ease` :기본값, 시작은 느리게, 중간은 빠르게, 끝은 느리게
* `linear` : 처음부터 끝까지 일정한 속도로
* `ease-in` : 천천히 시작해서 점점 빠르게
* `ease-out` : 빠르게 시작해서 점점 느리게