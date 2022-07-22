# 부트스트랩(bootstrap)

- 라이브러리(남이 만들어 놓은거를 들고옴)
- 반응형도 가능
- class 설정하면 bootstrap에 미리 설정해둔게 적용되는듯
- 필요할 때 bootstrap 들어가서 찾으면서 쓰면 될 듯
- 작동방법
	- get started
	- css 링크 복사해서 head에 저장
	- js 링크 복사해서 body 제일 끝에 저장
	- 사용하고 싶은 항목을 복사 붙여넣기
- 작동원리
	- 스타일이 적용되는 이유: 위에 css링크(CDN)를 이용하여 링크를 통해서 접속=링크에 있는 css를 사용하는 것

- grid(layout 항목에 있음)
	- 한줄(column)을 12개의 단락으로 나뉨
	- 예를 들어 <div class='col-lg-3 col-md-6 col-sm-12'>
	- offset-md-4 라는걸 사용하면 앞에 여백을 만들 수 있음
	- 전체 여백을 없에고 싶으면 container-fluid 사용

- 부트스트랩 무료 템플릿도 있음, 유료도 있고
- font awesome 에서 해당 아이콘의 이름과 모양을 알려줌, icon의 사용방법들이 나옴(class 복사 붙여넣기)
- toast
- summernote
- modal