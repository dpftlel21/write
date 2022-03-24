# 1. HTTP란?
## ⓐ Http(HyperText Transfer Protocol) 의미
- 인터넷 상에서 통신을 할 때 데이터를 주고받는 형식(프로토콜)들 중 하나를 의미하며 각 HTTP 요청과 HTTP 응답은 정해진 형식이 있습니다. 클라이언트가 HTTP 요청의 형식으로 서버에게 요청을 보내면 서버가 그 요청을 HTTP 요청의 형식에 맞게 해독을 하고, 이에 대한 응답을 HTTP 응답의 형식으로 클라이언트에게 보내면 클라이언트가 그 응답을 HTTP 응답의 형식에 맞게 해독을 하는 것입니다.

## ⓑ HTTP 특징
- HTTP 프로토콜은 상태가 없는 프토토콜 즉, 데이터를 주고 받기 위한 각각의 데이터 요청이 서로 독립적으로 관리 된다는 것을 의미합니다.

- 서버는 세션과 같은 별도의 추가 정보를 관리하지 않아도 되고, 다수의 요청 처리 및 서버의 부하를 줄일 수 있는 성능의 이점을 가집니다.

- HTTP 프로토콜은 일반적으로 TCP/IP 통신 위에서 동작하며 기본 포트는 80번입니다.

## ⓒ HTTP REQUEST(요청), HTTP RESPONSE(응답)
<img src="https://joshua1988.github.io/images/posts/web/http/request-response.png" width="500px">

- HTTP 프로토콜로 데이터를 주고받기 위해서는 아래와 같이 REQUEST(요청)을 보내고 RESPONSE(응답)을 받아야 합니다.

- 위 사진을 쉽게 이해하기 위해서 클라이언트와 서버를 알아야 하는데 여기서 클라이언트란 요청을 보내는 쪽이며 웹에서는 브라우저에 해당합니다. <br> 서버는 요청을 받는 쪽이고 데이터를 보내주는 원격지의 컴퓨터를 의미합니다.

## ⓓ HTTP 요청 메서드
- URL 구조

<img src="https://joshua1988.github.io/images/posts/web/http/url-structure.png" width="500px">

- 위 사진의 URL을 이용하면 서버에 특정 데이터를 요청할 수 있고, 요청하는 데이터에 특정 동작을 수행하고 싶을 때 HTTP 요청 메서드를 이용합니다.

- HTTP 요청 메서드는 HTTP Verbs라고 불리며 아래와 같은 주요 메서드를 가지고 있습니다. <br>
**㉮ GET :** 존재하는 자원에 대한 요청<br>
**㉯ POST :** 새로운 자원 생성<br>
**㉰ PUT :** 존재하는 자원 변경<br>
**㉱ DELEFTE :** 존재하는 자원 삭제<br>

  이와 같이 데이터에 대한 조회, 생성, 변경, 삭제 동작을 HTTP 요청 메서드로 정의합니다. 때에 따라서는 POST 메서드로 PUT, DELETE의 동작도 수행할 수 있습니다.

- 기타 요청 메서드도 있습니다.<br>
**㉮ HEAD :** 서버 헤더 정보 획득, GET과 유사하지만 Response Body를 반환하지 않음<br>
**㉯ OPTIONS :** 서버 옵션들을 확인하기 위한 요청, CORS에서 사용<br>