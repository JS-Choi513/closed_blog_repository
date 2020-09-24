---
layout: post
title: 데이터 통신 4주차 
description: "컴퓨터 공학과 3학년 2학기 데이터통신 강의내용 기록 "
modified: 2020-09-24
tags: [Data_Communication]
image: 
  path: /images/abstract-3.jpg
  feature: abstract-3.jpg
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
---

## 1.데이터 통신의 개요

### 1.3.데이터 통신의 구성요소 
* <strong>메시지</strong>: 통신의 목적이 되는 정보
* <strong>송신자</strong>: 메시지의 생성 및 송신을 담당하는 장치
* <strong>수신자</strong>: 전송매체를 통해 전송된 메시지를 수신하는 장치
* <strong>전송매체</strong>: 메시지가 송신자로부터 수신자에게 전달되는 경로
* <strong>프로토콜</strong>: 데이터 통신을 제어하는 약속 또는 규칙들의 집합

<figure class="half">
	<img src="https://user-images.githubusercontent.com/32115744/94139041-f8789d80-fea3-11ea-841f-fa3b9e4f1aaf.JPG" alt=""{: width="80%" height="80%"}>
 <center><figcaption>데이터 통신 시스템의 기본요소</figcaption></center>
</figure>

#### 1.3.1.데이터 통신 시스템의 구성요소

<figure class="half">
	<img src="https://user-images.githubusercontent.com/32115744/94139634-ee0ad380-fea4-11ea-8249-7bf0e4ff63b6.JPG
" alt=""{: width="80%" height="80%"}>
 <center><figcaption>데이터 통신 시스템의 구성요소</figcaption></center>
 </figure>


#### 1.3.2.데이터 통신관련 장비
<figure class="half">
	<img src="https://user-images.githubusercontent.com/32115744/94139862-5063d400-fea5-11ea-9b45-1dc969a236be.JPG
" alt=""{: width="80%" height="80%"}>
 <center><figcaption>장비의 구성</figcaption></center>
  </figure>

* <strong>데이터 단말장비(Data Terminal Equipment)</strong>: 데이터 수신장치나 데이터 송신 장치 또는 송수신 장치로 동작하며, 링크 프로토콜에 따라 행해지는 데이너 통신 제어 기능을 갖추고 있는 단말장치나 주 컴퓨터를 총칭
* <strong>데이터 통신장비(Data Communication Equipment)</strong>: DTE와 데이터 전송로 사이에서 접속을 설정, 유지, 해제하며, 부호변환과 신호변환을 위해 필요한 기능을 제공하는 장치를 총칭

> <strong>데이터 통신 시스템은 크게 데이터를 처리할 수 있는 데이터 처리계(컴퓨터)와 데이터를 전송할 수 있는 데이터 전송계(단말장비, 신호변환기, 전송매체, 통신제어장치)로 구성된다.</strong>


### 1.4.프로토콜의 정의

> <strong>Protocols define format. order of messages sent and received among network entities, and actions taken on message transmission, receipt</strong>

><strong>프로토콜(protocol)이란 데이터 통신에 있어서 신뢰성이 있고 효율적이고 안전하게 정보를 주고받기 위해 정보의 송/수신측 또는 네트워크 내에서 사전에 약속된 규약 또는 규범.
</strong>

범용적인 의미: 이종의 시스템 간에도 통신이 가능하게 하기 위해 만든 표준, 협약. 외교의례, 또는 의정서에서 유래했다.

#### 1.4.1 주요 요소
* <strong>구문(Syntax)</strong>: 데이터의 형식, 부호화, 신호레벨 정의 , 데이터 구조와 순서에 대한 표현 
예시) 어떤 프로토콜에서 데이터의 처름 8비트는 송신지의 주소를 나타내고, 다음 8비트는 수신지의 주소를 나타낸다. 


TIL

