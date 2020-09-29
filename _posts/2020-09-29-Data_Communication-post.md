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

> <strong>Protocols define format. order of messages sent and received among network entities, and actions taken on message transmission, receipt</strong>

><strong>프로토콜(protocol)이란 데이터 통신에 있어서 신뢰성이 있고 효율적이고 안전하게 정보를 주고받기 위해 정보의 송/수신측 또는 네트워크 내에서 사전에 약속된 규약 또는 규범.
</strong>

범용적인 의미: 이종의 시스템 간에도 통신이 가능하게 하기 위해 만든 표준, 협약. 외교의례, 또는 의정서에서 유래했다.

#### 1.4.1 주요 요소
* <strong>구문(Syntax)</strong>: 데이터의 형식, 부호화, 신호레벨 정의 , 데이터 구조와 순서에 대한 표현 
예시) 어떤 프로토콜에서 데이터의 처름 8비트는 송신지의 주소를 나타내고, 다음 8비트는 수신지의 주소를 나타낸다.
<a herf="https://tools.ietf.org/html/rfc791">protocal Request For Comment</a>: 통신프로토콜에 대한 약속, 논의등을 기록한 웹페이지 통신프로토콜에 대한 상세정보, 규약등이 명세되어 있다.
* <strong>의미(Semantics)</strong>: 각 비트가 갖는 의미를 나타내는 것으로 해당 패턴에 대한 해석과, 그 해석에 따른 전속제어, 오류수정 등에 관한 제어정보를 규정하는 영역  
* <strong>타이밍(Timing)</strong>: 두 객체 간의 통신 속도를 조정하거나 메시지의 전송시간 및 순서 등에 대한 특성을 가리킨다. 

#### 1.4.2 프로토콜의 목적
> <strong> 메시지 또는 데이터를 송신자가 수신자에게 보낼 때 정확(Accurate)하게(100%) 전달하기 위함</strong>
#### 1.4.3 프로토콜의 특징
* <strong>단편화와 재결합(Fragmentation and Reassembly)</strong>
* <strong>연결제어(Connection control)</strong>




