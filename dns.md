# 1. DNS와 작동원리

## ⓐ DNS가 무엇일까?

- 우리는 인터넷을 이용하여 검색이나 웹 서핑, 이메일 등을 사용할 때 도메인 이름(www.naver.com)을 웹 브라우저의 주소창에 입력하고 네이버에 접속 합니다. <br> 즉, 실제 naver.com 서버는 숫자로 구성된 IP 주소로 통신하지만, 우리는 기억이 쉬운 도메인 이름을 사용하는 것입니다.<br>
그럼 입력한 도메인 주소(www.naver.com)를 숫자인 IP 주소로 변환하는 과정이 필요한데 이를 담당하는 시스템이 **DNS** 입니다.

## ⓑ DNS를 왜 사용할까?

- 네이버나 다른 웹 싸이트에 접속하기 위해 인터넷창에 바로 해당 싸이트의 IP 주소를 입력하는 경우는 거의 없을 것일 뿐더러 길고 복잡한 IP 주소를 외우는 사람도 거의 없을 것입니다. <br>
→ 이렇게 길고 복잡한 IP주소를 외우기가 힘들기 때문에 문자 주소를 사용하기 위해 DNS를 사용하게 됩니다.

## ⓒ 구성 요소 및 동작원리

- **도메인 네임 스페이스(Domain Name Space) :** 최상위에 루트 DNS 서버가 존재하고, 그 하위로 인터넷에 연결된 모든 노드가 연속해서 이어진 계층구조로 구성됩니다.

- **네임 서버(Name Sever) :** 주소를 변환 시키기 위해 도메인 네임 스페이스의 트리구조에 대한 정보가 필요하고, 이 정보를 가진 서버 도메인 이름을 IP주소로 변환하는 것을 의미합니다.

- **리졸버(Resolver) :** DNS 클라이언트의 요청을 네임 서버로 전달하고 네임 서버로부터 도메인 이름과 IP 주소를 받아 클라이언트에게 제공하는 기능을 수행합니다.

## ⓒ DNS 동작과정
<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcgbNqc%2Fbtq1uuMDN4D%2Fcfifchk6rOn14ZyP9LB8O0%2Fimg.jpg">

1. DNS Query (from Web Browser to Local DNS) : "제가 원하는 웹 사이트의 IP 주소를 알고 계신가요?" Local DNS 서버에게 전달

2. DNS Query (from Local DNS to Root DNS) : "제가 원하는 웹 사이트의 IP 주소를 알고 계신가요?" Root DNS서버에게 전달

3. DNS Response (from Root DNS to Local DNS) : "저는 모르지만 , Com 도메인을 관리하는 네임서버의 이름과 IP 주소를 알려드릴 테니 거기에 물어보세요"

4. DNS Query (from Local DNS to com NS) : “ 안녕하세요. www. naver. com의 IP 주소를 알고 계신가요?"

5. DNS Response (from com NS to Local DNS) : "저는 모르지만 , Com 도메인을 관리하는 네임서버의 이름과 IP 주소를 알려드릴 테니 거기에 물어보세요"

6. DNS Query (from Local DNS to naver. com NS) : “ 안녕하세요. www. Naver .com의 IP 주소를 알고 계신가요?
 
7. DNS Response (from naver .com NS to Local DNS) : "저는 모르지만 해당 웹은 www. g.naver. com이라는 이름으로 통해요. g.naver .com 도메인을 관리하는 네임서버의 이름과 IP 주소를 알려드릴테니 거기에 물어보세요"

8. DNS Query (from Local DNS to g.naver. com NS) : “ 안녕하세요. www. g.naver. com의 IP 주소를 알고 계신가요?"

9. DNS Response (from g.naver .com NS to Local DNS) : " 네 www. g.naver .com의 IP 주소는 222.222.222.22와 333.333.333.33입니다"

10. DNS Response (from Local DNS to Web Browser) : "네 www. naver .com의 IP 주소는 222.222.222.22와 333.333.333.33입니다"

