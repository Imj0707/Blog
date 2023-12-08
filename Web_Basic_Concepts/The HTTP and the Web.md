🌐 HTTP 프로토콜: 웹 기반 애플리케이션 간 데이터 송수신을 위한 응용 계층 프로토콜
     - TCP/IP 기반임
     - HyperText Transfer Protocol

<img src="https://github.com/Imj0707/Blog/blob/main/Src/HTTP4.png" width = 400>

🤝 연결 방식: 요청-응답 주기 후에 컴퓨터 간 연결 종료, 응답 시 다시 연결되고 닫힘

📦 데이터 전송: 이미지, 비디오, 음악, 문서 등 다양한 데이터 전송 가능

🌐 Stateless: 클라이언트와 서버는 현재 요청 중에만 서로에 대해 알고 있음

🏗️ 웹 작동 원리: 클라이언트가 서버에 요청을 보내고, 서버가 응답을 준 후 연결 종료

📄 HTTP 메시지: 시작 라인, 헤더, 바디로 구성, 요청과 응답 메시지에 차이가 있음

<img src="https://github.com/Imj0707/Blog/blob/main/Src/HTTP1.png" width=400>

📡 요청 방식: 메서드(GET, POST 등), URI(자원 식별자), HTTP 버전으로 구성
ex) Request HTTP Message

<img src="https://github.com/Imj0707/Blog/blob/main/Src/HTTP2.png" width=500>

형식 : Method path/to/file.ext http/version

ex code ) GET /products/myproduct.html HTTP/1.0

👤 사용자 요청: 웹페이지 표시(GET 메서드) 등 서버에 명령을 전달

📑 응답 형식: HTTP 버전, 상태 코드(성공 또는 실패 여부 표시), 헤더, 응답 바디에 파일 포함

ex) Response HTTP message

형식 : http/version status code

(status code에는 익숙한 200, 404 등이 있음.)

ex code ) HTTP/1.0 200:OK

<img src="https://github.com/Imj0707/Blog/blob/main/Src/HTTP3.png" width=300>
