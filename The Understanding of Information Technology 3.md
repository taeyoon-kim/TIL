# 인터넷의 개요

### 인터넷

1. TCP/IP (Transmission Control Protocol / Internet Protocol 컴퓨터의 통신규약)에 기반을 둔 네트워크의 네트워크(A Network of Networks)

2. World Wide Web (WWW: 전세계에 퍼져 있는 거미 망)이라고도 부름

3. 인터넷의 연결
 - 하나의 네트워크를 담당하고 있는 주된 컴퓨터인 서버(Server)와 여러 개의 PC로 구성됨
 - 클라이언트(Client)는 통신 장치를 통해서 다른 네트워크에 연결
 - 한국에서 미국에 있는 친구에게 전자메일을 보내는 시점에서 가장 빠른 경로를 통해서 전달
 - 송신자는 이 과정을 전혀 고려하지 않아도 됨

```
LAN(Local Area Network) = Server + PC(Client) + PC + PC + ...

LAN = TCP/IP기반

Types of LAN
1. Bus타입 - 일직선상에 클라리언트와 서버가 물린 형태
2. Ring타입 - 가장 많이 쓰임. 원형 형태로 물린 서버와 PC들
3. Star타입 - 별모양으로 생긴 LAN 구조. 가운데가 서버. LAN의 네트워크상

정보는 메신저를 타고 이동하는데 토큰이라는 친구가 메신저를 업고다닌다.
Bus타입은 토큰이 좌우로, Ring타입은 원형으로, Star타입은 PC-Server-PC 로 움직인다.
```

- - -

# 인터넷의 역사

1. 다양한 네트워크
 - 1960년대부터 등장한 다양한 형태의 네트워크를 연결하여 자료와 정보를 공유할 수 있도록
표준화가 필요
 - 표준화를 위해 TCP/IP 프로토콜 통신규약을 제정
 - 유연성과 단순함이 인터넷을 전세계적인 네트워크로 발전시킨 원동력이 됨

2. 인터넷의 기원
 - 1960년대 말에서 1970년대까지 미국의 국방성이 추진한 알파넷(ARPANET)에서 찾을 수 있음
 - 1960년대의 동서 냉전은 미국과 소련이 서로 핵전쟁에서 우위를 차지하기 위해서 노력을
경주함
 - 알파넷은 알파(ARPA: Advanced Research Project Agency)가 특정 지역의 컴퓨터가 파괴되어도 다른 지역의 컴퓨터에서 네트워크를 이용할 수 있음
 - 다른 지역의 컴퓨터를 이용할 군사적인 목적으로 만들어짐

3. 알파 넷
 - 처음에는 군사적 목적으로 시작한 알파 넷은 미국내의 4개의 대학 만을 연결하는 컴퓨터 망
 - 1972년 일반인에게 공개되자 국방기술에 관련된 미국의 50여 개의 대학과 연구 기관 연결

4. 네트워크의 발전
 - 1984년 미국 국방성은 알파 넷을 순수연구용인 알파 넷과 군사용인 밀넷 (MILNET)으로 구분
 - 1987년에는 미국국립과학재단(NSF)은 알파 넷의 통신기술로NSFNET을 구축하여 학술연구용 네트워크로 발전시킴
 - 이 컴퓨터 망이 발전하여 인터넷이 됨

5. 인터넷 확장(1/3)
 - 인터넷이 확장됨에 따라 인터넷을 통한 메시지 교환도 증가
 - 월드 와이드 웹 프로토콜은 인터넷을 통해 하이퍼텍스트 및 그래픽의 효과적인 전송이 가능한 웹 브라우저(Web Browser)의 출현을 가능하게 함
 - **최초의 웹 브라우저인 모자이크(Mosaic)** 는 컴퓨터를 전혀 사용하지 못하는 일반인도 마우스를 이용하여 쉽게 인터넷을 사용할 수 있게 됨
 - 웹 브라우저의 시장도 발전을 거듭함. 모자이크(1993)와 네비게이터가 시장을 양분하다가 익스플로러(1995, 마이크로소프트)가 시장의 주도권을 유지함.
 - 오페라(1996), 사파리(2003, 애플), 파이어 폭스(2004, 모질라 재단), 크롬(2008, 구글) 등의 다양한 웹 브라우저가 출시됨.

6. 인터넷 확장(2/3)
 - 웹 문서를 작성하는 표준언어는 HTML(HyperText Markup Language)
 - 관련된 통신규약은 HTTP(HyperText Transfer Protocol)
 - HyperText는 음성이나 영상까지 링크할 수 있는 HyperMedia 로 발전하여 방송통신 융합이 가능함.
 - <u>최초의 HTML은 1980년</u>에, 확장된 표준인 HTML4.01(1999)을 거쳐 다양한 기능을 포함한 HTML5이 만들어짐.
 - W3C(World Wide Web Consortium)은 구글, 마이크로소프트, 애플 등과 손을 잡고 <u>HTML5</u>을 표준안으로 주도함(2014).
 ```
 사실 HyperText라는 표현은 HyperMedia라고 바뀌어야한다고 말씀하심.
 HyperMedia 가 Text에 Image, Video를 포함할 수 있기 때문
 ```

7. 인터넷 확장(3/3)
 - HyperText
 ```
 제한된 화면안에 많은 정보를 넣기위해 Icon을 클릭하면 팝업이 되며 다른 창이 띄워지는 것을 계층적 구조(Hierarchical Structure)라고 한다.
 HTML도 계층적 구조를 가지고있다.
 ```

8. 미국의 경우에 최초 500만 명의 가입자를 확보하는데 걸리는 시간
 - 전화 25년(1920-1945)
 - 라디오 38년(1922-1960)
 - 텔레비전 13년(1951-1964)
 - 케이블 10년(1976-1986)
 - 인터넷 5년(1993-1998)

- - -

# 인터넷의 원리

1. LAN (Local Area Network)
 - 대부분의 공 기관에서는 LAN 서버와 전용선이 구비되어 있음
 - 네트워크 상의 컴퓨터는 <u>IP(Internet Protocol)(인터넷 주소)</u> 주소를 부여 받고 있음
 - 웹 브라우저의 초기 설정을 할 때 LAN 카드의 종류, 사용되는 네트워크의 프로토콜과 IP 주소를 정확하게 입력하면 바로 인터넷에 연결됨
>LAN과 인터넷 백본(Internet Backbone)간에 전용선이 설치되어 있지 않은 경우
>>인터넷 서비스 제공자(ISP: Internet Service Provider)가 제공하는 **전용선** 을 임대하여 사용하는데, 빠른 데이터의 송수신이 가능

```
Digital Network(Backbone)--------(전용선)---------LAN

Internet Backbone Privider : ISP집합 안에 속함. Digital Network망을 관리. IP 주소, 경로 정보 관리
```
 - <u>IP(Internet Protocol) 주소</u> -> DNS(Domain Name System) : www.dongguk.edu ```도메인 네임을 입력하면 브라우저 내에서 IP 주소로 바꿔줌```
 >IPv4 (version 4) : 8 bit X 4 영역 = 32 bit, 2의 32승, 약 43억 개의 주소
 >
 >IPv6 (version 6) : 16 bit X 8 영역 = 128 bit, 2의 128승, 약 31조 개의 주소
 >
 >ICANN(Internet Corporation for Assigned Names and Numbers, 비영리민간기구)이 도메인 이름 관리
 >
 >2011년 06월 부터는 각국의 언어로 원하는 단어로 도메인을 정할 수 있음.

 - <u>사물인터넷(IoT : Internet of Things)</u> 으로 IP 주소의 급속한 증가.
 - 인터넷에 접속할려면 IP 주소가 있어야 함.

2. 모뎀 전화선
 - 주로 전화선을 이용한 모뎀 이용
 - <u>모뎀(Modem)</u>은 컴퓨터에서 처리한 0과 1의 디지털 데이터와 아날로그 데이터를 변환시키는 **Modulation(변조)** 과 디지털 데이터를 다시 아날로그로 변환하는 **Demodulation (복조)** 의 과정을 통해 인터넷 연결
 - 모뎀은 전화선의 아날로그 데이터와 컴퓨터의 디지털 데이터를 교환하기 위해 변조와 복조를 반복하여 통신이 가능하도록 함
 ```
 전화선은 구리선으로 이루어져있고 아날로그 신호만 처리할 수 있다.
 컴퓨터는 디지털 신호만 처리할 수 있다.
 하지만 우리는 전화선을 사용하여 인터넷을 이용하기위해 모뎀을 중간에 설치하였다.
 컴퓨터(디지털)에서 전화선(아날로그)으로 바꾸는 과정을 Modulation(변조),
 전화선(아날로그)에서 컴퓨터(디지털)로 바꾸는 과정을 Demodulation(복조)라고 한다.

  'MO'dultation 과 > 'DEM'odulation 의 앞자를 따서 "Modem(모뎀)"이라고 부른다.

 요즘은 아날로그로 안바꾸고 디지털로 보내서 디지털로 바로 받는다. 따라서 에러도 덜하다.
 ```

 ```
 전송속도
 1. 데이터 압축
 2. 오류 탐지
 3. 전송 방법
   - 전 방향방식(full-duplex mode, 데이터를 주면서 받기 가능) -> 훨씬 빠름
   - 반 방향방식(half-duplex mode, 데이터를 보낼 땐 보내는 것만, 받을 땐 받기만 가능)

 LTE : 1Gbps(1초에 1Gb, 실제 한국에서는 절반 정도 속도 냄)  (G = 10^9)
 전화선 : 4800bps
 모뎀 두개 연결 : 9600bps

 만배정도 빨라졌음을 알 수 있음
 ```

3. 온라인 서비스
 - 사용자들이 간편하게 사용할 수 있도록 다양한 프로그램 제공
 - 정보서비스 제공자로부터 서비스 계정(혹은 ID)을 부여 받고 사용료 지불
 - 컴퓨터가 인터넷에 연결되기 위해서는 하드웨어와 소프트웨어 필요
 - 컴퓨터 생산업체들이 만들어 내는 다양한 하드웨어 플랫폼과 소프트웨어에서 운용될 수 있는 <u>표준화된 연결고리인 Winsock(Windows Sockets) 프로그램으로 관련 생산업체가 동의한 표준화 된 인터페이스(Interface)</u>

유저 - 웹브라우저 - 윈속(Winsock(Windows Sockets)) - 네트워크장비 - 생산업체

>윈속: 망 네트워크를 통해 컴퓨터와 통신을 주고받게 하는 라이브러리
- - -

# 인터넷의 연결 방법

> 비동기방식(Asynchrous), Packet Switched, 패킷 방식, 라우팅기능
>
> =>Network 공유

1. TCP/IP(Transmission Control Protocol/Internet Protocol)
 - 패킷을 이용한 비동기 전송 방식
 - 쉽게 설명하면 전달하고자 하는 메시지가 잘게 쪼개진 패킷으로 구성
 - 패킷 전송 시 시간적인 차이를 두며 목적지에 전송되는 방식
 - 비동기 전송방식은 사용자들에게 정보이용에 더 많은 재량권을 줌

```
전화선 : 동기식(A와 B가 전화하면 타인은 A와 B의 전화선에 연결 불가능)
인터넷 네트워크 : 비동기식(A가 보낸 패킷, B가 보낸 패킷이 라인에 번갈아 올라감)
```

```
Line Sharing : A가 보낸 패킷, B가 보낸 패킷이 라인에 번갈아 올라가서
누구나 동시에 패킷 올리기 가능
```

2. 패킷(Packet)
 - 꾸러미라는 의미|
 - 전하고자 하는 메시지가 여러 개의 토막 혹은 꾸러미 형태로 나누어져 목적지에 보내짐
 - 그리고 다시 그 순서에 의해 합쳐짐

```
Type A Network(PC,PC,PC,....,PC -----서버)
[Type A 헤더, Payload]
｜
｜
인터넷(게이트웨이 - [Type B 헤더, Type A 헤더, Payload] - 게이트웨이)
｜
｜
Type B Network(서버----- PC,PC,PC,.....,PC)
[Type B 헤더, Type A 헤더, Payload]

1. 다른 네트워크상의 컴퓨터로 패킷을 보내기 위해 [Type A 헤더, Payload] 생성
2. 첫 번째 게이트웨이는 또다른 헤더를 첨가 -> [Type B 헤더, Type A 헤더, Payload]
3. 그 패킷을 수신한 네트워크 B는 패킷을 어떻게 전송해야 할지 안다.
```

```
패킷(Packet)의 구성
    -> 발신인 주소(IP주소), 수신인 주소(IP주소),패킷의 내용 및 유형, 패킷의 순서

    따라서 패킷이 비 동기적으로 도착을 했을 때, 조합을 하여 원래의 메세지를 알 수 있음

    네트워크 망을 공유하기 위해 패킷을 나누워 비동기적으로 보내는 것임을 알아야함.
```

- - -

# 인터넷의 사용속도

1. 인터넷으로 자료를 검색하거나 파일을 전송할 때 소요되는 시간은 각 컴퓨터와 <u>인터넷 백본</u>과의 연결된 매체의 대역폭(Bandwidth)과 직접적인 관련

2. 광섬유를 이용한 광케이블
 - 1초에 400 Gbps : 9만권 분량의 백과사전을 1초에 보낼 수 있는 용량
 - 전화선의 전송속도는 14.4 - 56 Kbps
 - 케이블 TV에 사용되는 동축케이블은 1.2 - 27 Mbps

3. 국내 인터넷 사용속도
 - 최근 **<u>FTTH(Fiber to The Home)의 보급으로 인터넷 사용속도가 Gbps급</u>** 으로 성장
 - 2012년 대한민국- 17.5Mbps
 - 세계 인터넷속도- 2.3Mbps
 - 통신속도: bps(bits per second), 1byte=8bits, K:10^3,  M:10^6,  G:10^9

- - -

# 인터넷과 인트라넷의 차이점

1. 인트라넷
>Intra : 내부  ///// Intranet : 내부망

 - 기업의 경영활동에 관련된 특수한 용도의 네트워크
 - 폐쇄적이고 제한된 용도의 정보를 제공하는 기업 내부의 네트워크
 - 영어의 인트라(Intra)는 내부 혹은 안쪽 의미
 - 인트라넷은 **<u>외부의 무단 접속을 차단하기 위해 방화벽(Firewall)<u>** 사용
 - 방화벽은 보안에 관련된 기술로써 주로 패스워드를 체크하거나, 해킹(Hacking)을 방지할 수 있는 소프트웨어 및 하드웨어
- 인트라넷의 활용: 그룹웨어(GroupWare), 기업내의 통신망, 그리고 기업간의 원활한 전자문서교환(EDI) 등에 사용

2. 인트라넷(Intranet) + 엑스트라넷(Extranet) = 인터넷(Internet)

- - -

# 엑스트라넷 - 협의

- 기업 내부의 특정 목적을 위한 네트워크에 대응하는 외부 협력업체 간의 네트워크
- 기업 간의 업무효율을 높이기 위해서 공급망관리(SCM: Supply Chain Management) 고객관계관리(CRM: Customer Relationship Management)를 지원하는 네트워크

- - -

# 학습정리

1. 인터넷의 개요
 - 인터넷: TCP/IP(Transmission Control Protocol/Internet Protocol: 컴퓨터의 통신규약)에 기반을 둔 네트워크들의 네트워크

2. 인터넷의 역사
- 1960년대에 시작해 알파넷과 네트위크의 발전을 거쳐 인터넷으로 확장됨

3. 인터넷의 원리
 - 1977년에 패킷 교환 프로토콜이 개발되었는데, 이것이 인터넷에서 통신의 기반이 된 TCP/IP

4. 인터넷의 연결방법
 - LAN (Local Area Network), 모뎀, 전화선

5. 인터넷 사용속도
 - 전화선의 전송속도는 14.4 - 56 Kbps, 케이블 TV에 사용되는 동축케이블은 1.2 - 27Mbps(Mega Bits Per Second: Mega는 1,000,000 배)

6. 인터넷과 인트라넷의 차이점
 - 기업의 경영활동에 관련된 특수한 용도의 네트워크

7. 엑스트라넷의 의미
