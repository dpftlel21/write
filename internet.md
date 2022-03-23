# 1. TCP/IP?

## ⓐ TCP/IP란?
* **TCP :** 클라이언트와 서버가 데이터를 주고 받을수 있게 하도록 지원하는 것이 TCP입니다. 즉, 클라이언트와 서버간에 데이터를 신뢰성 있게 전달하기 위해 만들어진 프로토콜로 이해하시면 됩니다.<br>
TCP는 근거리 통신망(LAN), 원거리 통신망(WAN), 인트라넷, 인터넷 등 컴퓨터에서 실행되는 프로그램 간에 데이터를 안정적으로 순서에 맞춰 에러없이 데이터를 교환할 수 있게 합니다.

* **IP :** 네트워크 상에서는 고유한 주소가 존재합니다. 컴퓨터 주소는 인터넷에 접속할때 컴퓨터 각각에 부여 받습니다.  
ex) 집 주소, 전화번호가 대표적인 사례입니다. 이 주소는  예를 들어서192.168.2.1 이런식으로 총 4바이트로 이루어져 있습니다.<br>
@ 만약 내 컴퓨터 주소가 궁금하다면 윈도우라면 cmd에서 ipconfig 유닉스 계열이면 ifconfig를 치면 주소가 나옵니다.

## ⓑ TCP/IP의 배경
* TCP/IP가 나타난 이유는 먼저 컴퓨터간의 통신을 위해서입니다.
* TCP/IP는 컴퓨터와 컴퓨터간의 지역네트워크(LAN) 광역네트워크(WAN)에서 원할한 통신을 가능하게 하기위한 통신규약으로 정의합니다. 최초는 ARPANET(최초의 컴퓨터)로 시작이 되었으며 미국방위통신청에서 컴퓨터간의 통신을 위해서 TCP/IP를 사용하도록 한것이 그 시초가 되었습니다.

## ⓒ TCP/IP 선택 이유?
* 하드웨어, 운영체제, 접속매체에 관계없이 동작할 수 있다는 점 때문에 인터넷 통신을 위한 핵심이 되었습니다.
* TCP/IP의 이름에서 알 수 있듯이 2개의 프로토콜이 이루어져 있습니다. IP 기반에 TCP가 사용되서 이렇게 불리어집니다. 즉, IP 프로토콜위에 TCP 프로토콜이 놓이게 된겁니다.

# 2. 인터넷?
## ⓐ 인터넷이란?
각 컴퓨터들간의 TCP/IP 통신 프로토콜을 이용해서 서로 데이터를 주고 받도록한 네트워크를 말합니다 혹은, 네트워크의 네트워크를 구현하여 모든 컴퓨터를 하나의 통신망 안에 연결하고자 하는 의도엣 인터넷이라고도 합니다.

## ⓑ 네트워크

**1. 단일 통신**


<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FdQgzYe%2FbtqTcQXEZmq%2FKb26sNOu1MnNRI9bQONtx1%2Fimg.png" > <br>
- 두개의 컴퓨터가 통신이 필요할때 저희의 컴퓨터와 다른 사람의 컴퓨터 물리적(케이블 선) 또는 무선(WiFi, Bluetooth)으로 연결이 되어야합니다. 이러한 방식으로 여러대의 컴퓨터를 연결을 할수는있습니다.

**2. 여러 컴퓨터의 통신**


<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcibDry%2FbtqS29c9Xfw%2FwflLiKKdsMbvar8XbLSVl1%2Fimg.png" width="350px">


- 보시는 것처럼 매우 난잡해 보이죠? 이런식으로 컴퓨터가 많이 연결되어 있으면 관리하기 힘들뿐더러 가독성도 떨어지게 됩니다.

**3. 라우터 이용 네트워크**


<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FzcfiH%2FbtqS1V7ksYm%2FJF2n5ssL6IBbm7uRmWtRvK%2Fimg.png" width="350px">


- 이러한 문제를 해결하기 위해 라우터가 등장했고 전 사진과 비교했을 때 매우 깨끗해진 것을 알 수 있습니다.

- 각 컴퓨터는 라우터라는 소형 컴퓨터에 연결 됩니다. 이 사진에서 컴퓨터가 하나의 10개의 플러그를 가지고 있는 라우터에 10대의 컴퓨터가 각 하나씩 가지고 있는 케이블로만 연결이 됩니다.<br>

- 라우터는 보기엔 많은 작업을 할 것 같지만 실제로는 데이터를 원하는 컴퓨터한테 데이터를 잘 전달해주는 간단한 작업을 합니다.

- A라는 컴퓨터가 B에게 메시지를 보내기 위해서는 라우터를 거쳐야 하며 라우터는 메시지를 B로 전달하고, 그 외에 상관없는 컴퓨터에는 보내지 않도록 합니다. <br>

**4. 라우터와 라우터간의 연결을 통한 네트워크의 네트워크**

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbtfgF6%2FbtqS1VlW2xI%2FNq7TWrcz9C5aIwTOIYYgp1%2Fimg.png">


- 이 방법도 몇백, 몇천대의 컴퓨터는 단일 컴퓨터로 확장이 불가능하며 라우터도 컴퓨터이기 때문에 컴퓨터처럼 라우터끼리 연결하여 네트워크 확장이 가능합니다.

**5.모뎀을 이용한 네트워크 연결**


<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fdk7h7I%2FbtqS295lORM%2FNGqb2QqcbRSBy3No7ns8M1%2Fimg.png" width="350px">

- 인터넷을 앞서 언급 했듯이 네트워크의 네트워크를 구현하여 모든 컴퓨터를 하나의 통신망의 연결하는 것이라고 정의했습니다. 이러한 네트워크가 인터넷에 가깝다고 하지만 아주 먼곳에 있는 지역과는 케이블 연결이 불가능합니다. 

- 전력 및 전화와 같이 집에 연결된 케이블, 전화 기반 시설은 세계 어느 곳과도 연결되어 저희가 원하는 네트워크 구성으로 되어 있었습니다.

- 네트워크를 전화 시설과 연결하기 위해 모뎀이라는 특별한 장비가 필요합니다. 

**6. 전체 네트워크 인프라**


<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fmk65I%2FbtqS29EeMIV%2FDWTGDmvx0JeBUCzzkcWWhK%2Fimg.png" width="350px" height="600px">

- 이 네트워크는 전화망에 연결되어 누가 어디에 있든 데이터를 주고 받을 수 있습니다.

- 데이터를 주고 받기 위해 네트워크를 인터넷 서비스 제공업체 ISP에 연결합니다.<br>
**ISP :** 모두 함께 연결되는 몇몇 특수한 라우터를 관리하고 다른 ISP의 라우터에도 엑세스를 할 수 있는 회사를 의미합니다. <br> 대표적인 사례로 LG U+, KT, SKR 등이 있습니다.

- 이 네트워크의 메시지는 ISP 네트워크의 네트워크를 통해 대상 네트워크로 전달됩니다. 인터넷은 이러한 전체 네트워크 인프라로 구성되고, ISP는 중간에서 데이터를 전달을 해 주는 역할입니다.







