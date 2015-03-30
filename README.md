# pro-angularjs
프로 AngularJS 소스 코드 정리.
> [BOOK] pro angularjs, Apress
> 원본 source download: http://www.apress.com/9781430264484?gtmf=s

시스템
- node.js -ver v0.12.0
- deployd

환경성정
- node.js 설치: https://nodejs.org/
- deployd 설치: http://deployd.com/
- Deployd 셋팅
  1) Sports Store 생성: dpd create sportsstore
  2) Dpd 실행: dpd -p 5500 sportsstore\app.dpd
  3) Dpd Dashboard 접속: http://localhost:5500/dashboard/
  4) products 컬렉션 생성
	name		string	required
	description	string	required
	category	string	required
	price		number	required

  5) orders 컬렉션 생성
	name		string	required
	street		string	required
	city		string	required
	state		string	required
	zip		string	required
	country		string	required
	giftwrap	boolean
	products	array	required
  5) users 데이터 생성
    *주의! Collection이 아닌 Users Collection으로 생성.
  6) products, orders 인증 추가
	아래 컬렉션 Event탭에
		products -> On Put, On Delete
		orders --> On Get, On Put, On Delete
		users --> None
	아래 스크립트 추가

	if (me === undefined || me.username != "admin") {
	    cancel("No authorization", 401);
	}

실행
- node run : http://localhost:5000/
- 

팁
- 2장 json 파일 IIS에서 서비스하기
  add .json handler support in II7
  1) Open IIS Manager
  2) Display properties for the IIS Server
  3) Click MIME Types and then add the JSON extension:
  4) File name extension: .json
  5) MIME type: application/json
* http://www.uipress.com/add-json-handler-support-in-iis-7/





