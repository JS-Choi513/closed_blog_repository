---
layout: post
title: 데이터 통신 7주차 
description: "컴퓨터 공학과 3학년 2학기 데이터통신 강의내용 기록 "
modified: 2020-10-13
tags: [Data_Communication]
image: 
  path: /images/abstract-3.jpg
  feature: abstract-3.jpg
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
---

## 4.데이터 통신의 기본개념

### 4.1 회선구성

#### 4.1.1 점대점(Point-to-point)방식
메인프레임 형태의 중앙의 컴퓨터와 여러 터미널들이    독립적인 회선을 이용하여 1:1로 연결되는 방식
비지능형 터미널을 비동기식으로 중앙 컴퓨터에 연결할 때 사용한다. TCP/IP 환경에서는 PPP를 사용하여 1:1로 연결

#### 4.1.2 다중점(Multi-point)방식
하나의 장치에 연결된 하나의 전용회선을 사용하여 다수개의 장치들을 연결하여 정보를 송수신하는방식, 멀티드롭(Multi-drop) 방식이라고도 함

  <figure>
	<img src="https://user-images.githubusercontent.com/32115744/95880973-09397680-0db3-11eb-832c-f5a3146a817d.png" width="80%" height="80%">
 <center><figcaption> Point-to-point vs Multi-point</figcaption></center>
</figure>

#### 4.1.3 교환(Switching)방식
* <strong>회선교환 방식(circuit switching)</strong>
정보 전송 시작 시 물리적인 연결을 확립하고 전송이 종료될 때까지 연결유지, 물리적으로 연결된 회선은 다른사람과 공유 불가, 초기 전화시스템은 교환원이 직접 회선을 연결하여 음성통신이 가능하게 했다.
특징
   * 전송 중 항상 동일한 경로를 경우하여 데이터 전송
   * <strong>점대점 방식의 전송구조를 갖는다</strong>
   * 상대적으로 긴 접속 시간을 필요로 하나 전송지연은 거의 없다. 
   * 고정적인 대역폭을 사용한다.
   * 속도나 코드의 변환이 불가능하다.
  <figure>
	<img src="https://user-images.githubusercontent.com/32115744/95883444-e6f52800-0db5-11eb-87da-e46ba37cd362.jpg" width="100%" height="80%">
 <center><figcaption> Circuit Switching</figcaption></center>
</figure>

* <strong>패킷교환 방식(packet switching)</strong>
패킷 마다 주소를 삽입, 노드들이 패킷을 통하여 대역폭을 공유하는 방식이다. 패킷의 주소를 보고 최종 목적지 까지 패킷을 전달한다. 데이터 트래픽이 없을 때 낭비되는 대역폭을 효율적으로 사용할 수 있으며 물리적인 전송로를 여러 노드가 공유한다. 
패킷스위칭에는 Datagram, 과 Virtual Circuit 방식이 있다.
    <figure>
	<img src="https://user-images.githubusercontent.com/32115744/95883521-fffdd900-0db5-11eb-86ec-491cfb82fcd2.jpg" width="100%" height="80%">
 <center><figcaption> Packet Switching <figcaption></center>
</figure>
&nbsp;  &nbsp;  &nbsp;  &nbsp;특징

   * 주로 데이터를 위한 교환방식으로 대역폭의 효율적인 이용이 목적이다.
   * 교환기 자체의 비용을 낮출 수 있다.
   * 패킷교환기는 컴퓨터 그 자체이며 교환행위는 컴퓨터 메모리의 어떤 부분에 있는 데이터를 다른 메모리 위치로 옮기는 컴퓨터의 명령어에 의해 수행되므로 소프트웨어에 의한 교환이라고 볼수 있다.

   * <strong>DataGram 방식(Indivisual Routing)</strong>
   컴퓨터 통신의 기본단위이다. 패킷마다 주소를 넣어 구성하고 패킷을 독립적으로 취급한다. 따라서 재조합하는 기능이 요구된다. 송신자의 패킷 순서와 수신자의 패킷순서가 다를수 있다 손실시 송/수신자에서 복구를 제어한다. 호 설정 절차가 필요없고 적은양의 데이터를 전송할 때 효율적이다. 

   * <strong>Virtual Circuit 방식</strong>: VCI(virtual circuit identifier)라는 수치를 이용하여 전송한다. 전송을 시작할 때 두 지점 사이의 논리적 전송경로를 설정(connection establishment)한다. 송수신자 주소 대신에 논리적인 전송경로 번호를 이용하여 스위칭한다. <strong>회선교환방식의 회선과 유사하다.</strong>
   각 패킷은 데이터정보 분만 아니라 가상회선 식별자(VCI)를 포함한다. 경로설정과 관련되 결정을 할 필요가 없다. 패킷의 순서 및 오류제어를 망에서 제공한다. 데이터그램 방식보다 속도가 더 나을 수 있다.(회선을 소프트웨어적으로 고정)  


### 4.2 전송기술의 종류와 특성

#### 4.2.1 단방향과 양방향 전송
* <strong>단방향 전송방식(Simplex)</strong>: 데이터의 전송로에서 한 방향으로만 데이터가 흐르는 전송방식(라디오, TV 등)
데이터는 컴퓨터측에서 제어를 받는 장비측으로 전송
* <strong>양방향 전송방식(Duplex)</strong>: 방향의 전환에 의해 데이터의 흐르틑 방향을 바꾸어 전송가능, 송수신측이 정해져 있지 않다. 
   * <strong>반 이중 전송방식(Half duplex)</strong>: 두 장치 간에 교대로 데이터를 전송(무전기) 한 순간에 반드시 한쪽으로만 전송
   * <strong>전 이중 전송방식(Full duplex)</strong>: 두 장치 간에 동시에 양방향으로 데이터를 교환한다. 전송회선의 사용효율이 높고 회선비용이 많이 소요된다. 

#### 4.2.2 아날로그 및 디지털 전송
* 아날로그 전송방식: 아날로그 신호를 수단으로 전송한다. 음성이나 변조된 디지털 데이터 등을 의미하고 전송거리 증가에 따른 신호감쇄를 막기위해 증폭키를 사용한다. 
* 디지털 전송방식: 디지털 신호를 전송하는 수단, 제한된 거리에서의 감쇄현상은 없으나 전송거리의 제한을 극복하기 위해 리피터 사용

#### 4.2.3 직렬 전송과 병렬 전송
* 직렬 전송 방식: 한번에 한 비트씩 순서대로 데이터 전송, 쉬프트 레지스터를 사용하여 전송한다.
* 병렬 전송 방식: 여러개의 비트를 그룹(워드, 바이트)으로 한번에 전송, 패리티 또는 제어비트 전송을 위해 추가적인 전송을 필요로 한다. 전송속도가 빠르다. 

#### 4.2.3 비동기 및 동기 전송
* 비동기식 전송(비트전송): 데이터는 짧은 비트열로 나뉘어 전송한다. 각 전송 비트열 내부에서 동기화를 유지한다. 비트열 전후에 시작비트(ST bit)와 정지비트(SP bit)를 추가한다.
* 동기 전송 방식(비트블록 전송): 문자 또는 비ㅌ들의 데이터 블록 단위로 송수신한다. 데이터 블록의 전후에 제어정보를 삽입한다. 데이터와 제어정보를 합쳐서 프레임 이라고 한다. 전송효율 및 전송속도가 높다.
  * 비트 전송방식: 데이터 블록을 플래그를 사용하여 구분한다.
  플래그: 데이터 블록의 전후에 추가되어 블록의 시작과 끝을 나타내는 특별한 비트패턴
  * 문자 전송방식: 특정 문자를 이용하여 동기화 수행, 전송 데이터도 문자 단위로 취급한다. 
  <figure>
	<img src="https://user-images.githubusercontent.com/32115744/96161010-b1854180-0f51-11eb-9149-a3c59e686671.JPG" width="80%" height="80%">
 <center><figcaption> 문자전송방식</figcaption></center>
</figure>

