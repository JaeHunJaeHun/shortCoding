# HTTP 웹 기본지식(1)

## 인터넷 프로토콜 역할
* 지정한 IP 주소(IP Address)에 데이터 전달
* 패킷(Packet)이라는 통신 단위로 데이터 전달

## IP 패킷 정보
전송 데이터를 감싸는 IP패킷의 정보
* 출발지 IP
* 목적지 IP
* 기타 ...
> 전송 데이터를 감싼 클라이언트 패킷을 서버에 전달 (여러 노드를 거쳐서 서버에 전달)
> 서버 패킷은 최적의 길로 클라이언트에게 전달이 된다.

## IP 프로토콜의 한계
1. 패킷을 받을 대상이 없거나, 서비스 불능 상태여도 패킷을 전송한다.
2. 중간에 패킷에 사라져도 모른다.
3. 패킷이 여러 노드를 거치면서 순서대로 오지 않을 수 있다.
4. 같은 IP를 사용하는 서버에서 통신하는 어플리케이션이 둘 이상일 때 구분이 힘들다.

## TCP UDP
인터넷 프로토콜 스택의 4계층
* 애플리케이션 계층 - HTTP, FTP
* 전송 계층 - TCP, UDP
* 인터넷 계층 - IP
* 네트워크 인터페이스 계층

## 메시지 전송 순서
1. 프로그램에서 메시지를 보내게 되면
2. SOCKET 라이브러리를 통해 TCP로 전달
3. TCP 정보 생성하여 전송데이터를 감싼다.
4. IP 패킷 생성하여 감싼다.
5. 네트워크 인터페이스에서 LAN카드를 통헤 서버로 전송

## TCP/IP 패킷 정보
* 출발지 PORT
* 목적지 PORT
* 전송제어
* 순서
* 검증 정보 등

## TCP 특징
전송 제어 프로토콜(Transmission Control Protocol)
* 연결 지향 - TCP 3 way handshake (가상 연결)
* 데이터 전달 보증
* 순서 보장
* 신뢰할 수 있는 프로토콜
* 현재는 대부분 TCP 사용

## TCP 3 way handshake란
1. SYN : 클라이언트 -> 서버 클라이언트가 서버에게 SYN 전송
2. SYN+ACK : 서버 -> 클라이언트  SYN을 받았다고 ACK와 함께 클라이언트로 전송
3. ACK : 클라이언트 -> 서버 SYN을 받았다고 ACK 전송

## UDP 특징
사용자 데이터그램 프로토콜(User Datagram Protocol)
* 기능이 거의 없음 -> 커스터마이징이 쉬움
* 데이터 전달 및 순서가 보장되지 않지만 빠름
* IP와 거의 같고 Port 체크섬 정도만 추가되어 있음
* 애플리케이션에서 추가 작업이 필요
* 점유율이 높아지는 중

## PORT
같은 IP에서 하나의 서버에 두개 이상을 연결해야 할 때 포트를 사용하게 되면
프로세스를 구분할 수 있다.
* 0 ~ 65535 할당 가능
* 0 ~ 1023 잘 알려진 포트, 사용하지 않는 것이 좋음
* FTP - 20, 21
* TELNET - 23
* HTTP - 80
* HTTPS - 443

## DNS
도메인 네임 시스템(Domain Name System)
* 전화번호부
* 도메인 명을 IP 주소로 변환

## DNS 사용
1. 도메인 명 google.com -> DNS 서버로 전송 (NS 서버에는 도메인 명과 IP의 정보가 저장되어 있음)
2. DNS 서버에서 IP 정보를 클라이언트에게 전달
3. 클라이언트는 IP 정보로 서버에 접속


참조 : [인프런] 모든 개발자를 위한 HTTP 웹 기본 (김영한)
