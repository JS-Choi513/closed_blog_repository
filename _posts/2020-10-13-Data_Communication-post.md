---
layout: post
title: 데이터 통신 7주차 
description: "컴퓨터 공학과 3학년 2학기 데이터통신 강의내용 기록 "
modified: 2020-10-13
tags: [Data_Communication]
image: 
  path: /images/DC.jpg
  feature: DC.jpg
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
---

## 1.데이터 통신의 개요


#### 1.4.4 프로토콜의 구성
* <strong>프로토콜의 계층화(Hierachy)</strong>: 상위 계층과 하위 계층으로 분리된 계층상에서 인접 계층간의 서비스의 이동
* <strong>계층적 독립성</strong>: 한 계층의 내부적인 변화가 다른 계층의 변화에 영향을 주지 않음 
* 상위 계층은 사용자가 통신을 쉽게 이용할 수 있도록 도와주는 역할(EDI, FTP emd):
* 하위 계층은 실제 통신의 효율적이고 정확한 전송을 담당하는 역할

#### 1.4.5 네트워크 프로토콜의 종류
* <strong>SNA</strong>: IBM사가 개발, 컴퓨터 통싡망 구조와 체계
7개 계층으로 구성, OSI 기본참조 모델과 호환성 x
* <strong>TCP/IP(Transmission Control Protocol/Internet Protocol</strong>: 미국 국방부에서 개발한 프로토콜 TCP와 IP를 조합, 4계층으로 구성한 것으로 현태 인터넷에서 사용됨 RFC(Request For Comments) 형태로 공개
* <strong>OSI(Open System Interconnection)</strong>: 국제 표준화 기구에서 제정한 국제적 표준화 망 구조, 7계층의 기본참조모델 제정, 다른 기종간의 상호 접속을 가능케 하는 표준 개방형 통신망에 대한 제반 사항을 규정
  <figure>
	<img src="https://user-images.githubusercontent.com/32115744/95876625-3899b480-0dae-11eb-8c01-e09c16e3fa52.png" width="80%" height="80%">
 <center><figcaption> OSI 7 Layer vs TCP/IP</figcaption></center>
</figure>

### 1.5 표준기구/표준안
> <strong>표준(Standard): 최적한 사회이익의 증진을 목적으로 해서 과학 기술 및 경험의 종합적 결론이라 이해관계자의 협력과 모든 의견, 대다수의 승인에 의해서 작성된 기술 사양서(technical specification) 또는 그 외의 문서</strong>   

표준은 정확하고 효율적인 통신을 위해서 필요하고 표준을 제정하는 여러 표준안과 기구가 존재한다.

* <strong>국제표준기구(ISO)</strong>
현재88개국의 국가표준단체로 구성되어있고 전세계 표준화 및 관련활동 개발을 촉진한다. OSI 모델을 제정

* <strong>국제전기통신 표준화 부문(ITU-T)</strong>
1956 창설된 CCITT의 후신
189개의 회원국이 있으며전기통신에 관련된 국제협야그 표준을 제정한다. 전화전속, 교환, 신호방법, 잡음에 대한 여러 표준 제정

* <strong>미국 국립표준기구(ANSI)</strong>
미국의 규격공업 표준을 제정, 국제 표준화기구의 미국대표

* <strong>전기전자공학자 협회(IEEE)</strong>
1963년 미국전기학회와 무선학과의 합병으로 생김, 세계 최대의 전기, 전자, 전기 통신, 컴퓨터 분야의 전문가 단체(컴퓨터과학 부문에서는 ACM이 있음)
IEEE 802 표준안: 현재 널리사용되고 있는 LAN 권고 표준안이다. IEEE 802.3(이더넷) IEEE 802.11(무선랜) 등

* <strong>전자산업 협회(EIA)</strong>
1924년 RMA로 창설, 정보통신분야로 일반적 전기특성, 데이터 통신, 수치제어 등에 관한 표준
RS-232-C: 단말장치와 모뎀간의 인터페이스 규정 

* <strong>ITEF</strong>
1986년 설립된 IAB 산하 조사위원회, 인터넷 운영, 관리 및 기술적 쟁점 등에 대한 해결을 목적, 

* <strong>RFC</strong>
ITEF에서 발표하는 인터넷 기술과 관련된 공식 기술 문서
인터넷 표준, 사양, 프로토콜, 단체들의 통보, 개인적인 의견에 관한 정보제공 RFC 문서로 등록 시 규약에 따라 번호가 붙여짐 RFC 959 : FTP 등

* <strong>KS/KICS 표준</strong>
한국 산업표준: KS
한국 정보통신 표준: KICS

