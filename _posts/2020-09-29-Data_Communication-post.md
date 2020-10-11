---
layout: post
title: 데이터 통신 5주차 
description: "컴퓨터 공학과 3학년 2학기 데이터통신 강의내용 기록 "
modified: 2020-09-29
tags: [Data_Communication]
image: 
  path: /images/abstract-3.jpg
  feature: abstract-3.jpg
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
---

## 1.데이터 통신의 개요


### 1.4.프로토콜의 정의

#### 1.4.3 프로토콜의 기능
* <strong>단편화와 재결합(Fragmentation and Reassembly)</strong>
단편화: 응용계층의 연속적인 비트 스트림 메시지를 하위 계층에서는 작은 블록으로 나눈다. OS에서 디스크에 파일을 저장할때 플래터에 차곡차족 저장되는데 중간에 파일을 삭제하거나 하면 디스크에 빈공간이 생기면서 공간을 낭비하게 된다. 이런 경우를 방지하기 위해 일정크기의 블록단위로 쪼개서 저장하거나 읽어오는것을 Fragmentation이라고 한다. 하지만 읽어올때 데이터가 분산되어있으므로 성능이 떨어질 수 있기 때문에 OS가 데이터를 모으는데 이를 Dfragmentation이라고 한다. 
재결합: 단편화 된 데이터를 받아 다시 하나로 합치는 기능 
* <strong>연결제어(Connection control, Connection Establishment)</strong>
비연결형 데이터 전송: 데이터를 송수신하는 개체간의 논리적인 연결없이 데이터를 전송(예: Datagram)
연결형 데이터 전송: 데이터를 송수신하는 개체간에 논리적 연결을 맺은 후 데이터 전송(예: virtual circuit) 
연결제어는 물리적으로 직접 연결을 제어하는 방법과 소프트웨어적으로 연결을 제어하는 방법이 있다. 
  * Circuit Switching: Call setup(Connection Establishment), 물리적 제어, 가용할 수 있는 리소스의 한계만큼만 사용할 수 있다 안정성과 성능을 보장한다. 
  *  packet Switching: Indivisial Routing,TCP(Connection Oriented), 소프트웨어적 제어 많은 사람이 한번에 사용할 수 있지만 이용자가 많아지만 안정성과 성능이 떨어진다. Sharing 이 주요 목적, 소프트웨어적으로 구현한다. 패킷이 전송이 되면 중간라우터가 IP 헤더를 보고 전송되어야 할 링크를 지정한다. 따라서 같은 회선에 서로 종류가 다른 패킷이 전송된다
  <figure>
	<img src="https://user-images.githubusercontent.com/32115744/95188216-14b2fd80-0807-11eb-8bdf-642c8f710d78.png" width="80%" height="80%">
 <center><figcaption>TCP/IP 3-way hand shaking</figcaption></center>
</figure>
송신자와 수신자 간 데이터 전송을 하기 전 통신에 연결확인을 3번한다. 
연결을 종료할 때는 2-way로 한다. 

* <strong>흐름제어(Flow control) </strong>
송신측 개체간의 데이터 양이나 속도를 조절하는 기능
송신측과 수신측의 속도차이나 네트워크 내부 문제 등으로 인한 정보유실(packet loss) 방지  
-Flow Control: 송신자가 네트워크 이상을 판단하여 속도제어
-Conjestion Control: 수신자가 일부러 ACK 를 전송하지 않아서 송신자가 전송속도를 줄이도록 만들거나 네트워크가 패킷을 누락(packet drop)시켜  속도를 제어한다. 기본적으로 두가지 제어가 상호작용하여 속도를 제어한다. 
  * 정지-대기(stop-and-window)흐름제어
  수신측의 확인신호(ACK)를 받기 전에 데이터를 전송하지 않음
  * 슬라이딩 윈도우(sliding-window)기법
  확인신호를 수신하기 전에 데이터의 양을 미리 정해주는 기법
  정지-대기 흐름기법보다 발전된 방법 
  초기에 수신자가 확인하기 전까지 보낼 수 있는 최대 패킷 수(window size)를 정하면 해당 패킷 수 만큼 수신자가 확인하지 않아도 전송 할 수 있다. 각 패킷에는 번호가 지정되고 수신자는 ACk 신호로 패킷 번호 하나를 보내는데 ACK 신호를 받은 송신자는 수신자가 패킷 번호 이전의 패킷은 성공적으로 받았다고 판단하고 그 다음 패킷부터 전송한다. 

* <strong>에러제어(Error control) </strong>
정보 전송 시 채널이나 네트워크 요소의 불완전성으로 데이터나 제어 정보가 파손되는 경우에 대히하는 기법 (정보를 반복적으로 overhead 전송한다.
  * Error Detection (예: parity, CRC...)
  사전에 송신자와 수신자 사이에 Error Detection 에 대한 프로토콜이 정의되어 있어야 한다. 
    -순환 잉여도 검사(CRC) 다항식 코드를 이용하여 오류검출 
    미리 약속된 수식을가지고 데이터를 계산하여 나머지가 0이면 오류가 없다고 판단한다. 
  * Error Correction (예: Hamming Code...)  
* <strong>동기화(Synchronization) </strong>
두 개체 사이에 정보를 송수신할 때 초기화 상태, 종료 상태 등의 동기를 맞추는 것, 송수신 간 서로 한 비트의 시간 길이가 다르면 전송된 신호를 유효한 정보로 변환 할 수 없다.

* <strong>순서화(Sequencing) </strong>
데이터를 단편화 하여 전송할 때 데이터들이 올바른 순서로 전송되기 위하여 필요한 기능, 연결 중심의 데이터 전송에만 사용한다. 






