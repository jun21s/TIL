# html

## Hyper Text Markup Language

### `<안에 명령어를 적어야 하는데 markdown도 영향을 받아서>` <br>모든 명령어 앞 뒤에다가 `을 붙여서 작동하지 않게 함

- html 문서를 실시간으로 보고 싶을때는 live server을 사용하여 저장하면 바로 반영되게 하면 작업하기 편함

- html은 웹페이지에 명령을 하는 것

- 확장자는 .html

- 메모장 사용하여 저장할때는 모든 파일에 utf-8로 하고 저장

- 강조하고 싶을 때는 `<strong>아아아</strong>`
  <br>

- 굵고 큰 문자를 만들고 줄 을 변경 하고 싶으면 `<h1>ddd</h1>`aaa하면
  ddd(강조)
  aaa

- `<h2>`로 하면 조금 더 작은 글씨

- 링크 넣는법

      - `<a href="인터넷주소">아아아 </a>`

  -여기서 a의 뜻은 anchor의 약어

- 새로운 탭이 열리면서 페이지가 열리게 하는법

      - `<a href="인터넷주소" target="\_blank">아아아 </a>`

  - target과 href의 순서는 상관없음
    - `<a target="\_blank" href="인터넷주소" >아아아 </a>` 이래도 됨

- 마우스를 올렸을때 설명을 미리하고 싶으면

      - `<a target="\_blank" href="인터넷주소" title="주소설명" >아아아 </a>`

- 목록을 만드는 법list

      - `<li>`아아아아`</li>`

- 그룹핑 하는법 unordered

  - `<ul>`
  - `<li>1</li>`
  - `<li>2</li>`
  - `</ul>`

  - `<ul>`대신에`<ol>`하면 숫자로 표시해줌older

- html도 heading 숫자로 표현 가능

      - `<h1>` `</h1>`
      - `<h2> </h2>`

- 페이지 자체의 제목을 설정해 주고 싶으면 `<title>ㅁㅁㅁ </title>` 하면 웹 페이지 자체의 이름을 ㅁㅁㅁ이라고 설정해줌

- 글씨가 깨지면

      - `<meta charset="utf-8">`

  을 해주면 됨

- 본문이 아닌 테그(title 테그, meta테그)

      - `<head>`...`</head>`

- 본문인 테그

      - `<body>`.... `</body>`

- 제일 처음과 끝에는

      - `<html>`...`</html>`

  해줘야 됨

- `<!DOCTYPE html>`을 시작할 때 무조건 써줘야 됨(document type declaration) 과거에 테그들이 바뀌는 경우들에 대비해서 미리 설정 해둔건데 고착화 되어 있어서 그냥 저걸로 고정됨

- 페이지에서 눌렸을 때 해당되는 장면으로 바뀌게 링크 넣어 놓는법
  - 해당 부분에 링크(1.html)를 미리 작성 해놓음
  - 여러가지 링크에 넣어둬야되는 페이지들을 작성해둠
  - 파일 이름을 링크(1.html)로 만들어 놓음

`<html>`<br>
`<head>`<br>
`<title>`<br>
`<body>`<br>
`<a>`<br>
`<img>`이미지 삽입<br>

`<meta>`글 안깨지게<br>
`<br>` 줄바꿈<br>
`<table>` 표<br>

`<p>`단락구분 <br>

`<script>` 자바스크립트<br>
`<div>` 브루핑? 그루핑?<br>

`<p>`태그 설명paragraph

- 줄바꿈과 여백을 넣으면서 단락 구분 - `<p>` `</p>`

  - `<br>`을 추가하면 좀 더 단락을 구분 시켜 줄 수 있음

- `<br>`태그 설명

  - 줄바꿈
  - 중복하면 간격이 더 늘어남
  - `<br>`태그는 따로 시작과 끝을 안해줘도 됨=`</br>`이거 없음

- `<img>`

  - 이미지 삽입
  - `<img src="이미지 이름.확장자">`
  - 크기를 바꾸고 싶으면 `<img src="이미지 이름.확장자" width="숫자">` 숫자는 픽셀로 계산
  - `<img src="이미지 이름.확장자" width="숫자" alt="설명">` alt는 이미지가 깨지면 원래 뭐 였는지 설명을 해줌 alternatice text
  - `<img src="이미지 이름.확장자" width="숫자" alt="설명" title="설명">` 마우스를 갖다대면 설명이 드러나게 함

- `<table>`은 처음과 끝에 해둬서 이게 테이블 이라는 것을 표시해줌

  - `<td>`는 table data
  - 항목 하나하나에다가 `<td>`내용`</td>`다 해줘야됨
  - 같은 행들을 그루핑 시킬려면 `<tr>`..... `</tr>`을 해야됨 그러면 한 줄 생성
  - 그 후에 전체 태그를 `<table>`....`</table>`로 해줘야됨
  - `<table border="숫자">` 숫자 에 따라서 테두리의 크기를 결정함
  - `<thead>`....`</thead>` 안에 있는 `<td>`를 `<th>`로 변형 가능

  - `<tbody>`....`</tbody>` 테이블도 바디와 헤드가 있음
  - `<tfoot>`....`</tfoot>` 하면 어디에 작성하든지 표 상에서 가장 아래쪽으로 자동으로 내려감, `<thead>`또한 마찬가지

- 테이블 병합하는법 - `<td rowspan="숫자">` 숫자 안에 있는 개수 만큼 병합됨(세로병합) - `<td colspan="숫자">` 숫자 안에 있는 개수 만큼 병합됨(가로 병합) - 병합했으므로 병합되어서 사라진 항목은 없에 놓음

- `<form>`

  - 처음과 끝네 `<form>`...`</form>`
  - `<form action="주소">` 하면 주소 부분에 적혀있는 곳으로 이동됨
  - `<p>`...`</p>` 하면 아이디 비번 입력창 만들 수 있음
  - 데이터 입력 창은 `<input type="내용">` 내용에 password 하면 숨김 가능
  - 제출 칸 만들고 싶으면 `<input type="submit">`
  - `<textarea`>하면 여러줄 입력 가능

- `<option>`, `<select>`

  - option과 select를 같이 써서 사용
  - `<option value="내용">`
  - 다중 선택 하고 싶을 때는 `<select ... multiple>` (근데 여기서 다중 선택 할 때는 ctrl 눌리고 마우스 좌클릭 해야됨)

- `<radio>`, `<checkbox>`

  - `<radio>`는 선택 할 수있는 동그란 버튼 생성
  - 하나만 선택 가능 하게 하고 싶으면`<input type="radio" name="1">` name을 같은걸 쓰면 됨
  - checkbox는 같은 이름이어도 다중 선택 가능

  - 둘다 <............. checkde>를 하면 그게 선택된 상태로 화면이 나옴(화면에서 클릭하면 바꿀 수 있음)

- `<button>`

  - `<input type="submit" value="전1송">`이렇게 해 놓으면 전1송이라고 버튼이 생기고 그걸 눌리면 `<form action="음음음">` 음음음 이라는 곳으로 이동됨
  - `<input type="reset">`버튼은 사용자가 입력한 모든 정보를 리셋시킴

- `<hidden field>`

  - `<input type="hidden" name="hide" value="egoing">`이렇게 해놓음
  - ui가 없지만 서버로 값을 전송하는 걸 원하면 input type에 hidden 을 해놓으면 됨. 이런게 있다만 알아두자

- `<label>`
  - `<label for="id_txt">`id`</label>` id가 무슨 의미인지 기입하는 거고 그 밑에 `<input id="id_txt" type="text" name="id" value="default value">`에도 id를 넣어놔야함
  - 위에 해놓은 걸로 하면 앞에 text 칸에 마우스를 클릭하면 커서가 그 안에 입력창으로 자동 이동됨
  - `<label><input type="checkbox" name="color" value="red">`빨강`</label>` 이렇게 하면 빨강 이라는 글자를 눌려도 체크가 됨
