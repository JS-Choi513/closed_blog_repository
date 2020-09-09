---
layout: post
title: 데이터 통신 1주차 
description: "컴퓨터 공학과 3학년 2학기 데이터통신 강의내용 기록 "
modified: 2020-09-09
tags: [Data_Communication]
image:
  path: /images/abstract-3.jpg
  feature: abstract-3.jpg
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
---

교재: 정진욱 지음, 데이터 통신, 생능출판
강의 후 복습겸 강의내용 기록을 위한 포스팅입니다. 잘못된 내용이 있으면 지적 부탁드립니다. 

#데이터 통신의 개요

##데이터와 정보 란?
**데이터: 현실세계로부터 단순하게 관찰이나 측정을 통해 수집한 사실을 숫자나 문자, 기호등으로  표현한 것**   
**정  보: 어떤상황에 대해 의사결정을 할 수있게 하는 지식**  
즉, 어떤상황에서 판단을 내리는데 필요한 데이터를 정보라고 한다. 

**통  신: 정보 제공자와  정보 수요자 간의 정보의 이동현상**
관점에 따른 통신의 분류
    |        분류관점      |   통신의 종류                                          |
    |:-------             |:-      ------:                                        |     
    |  전송매체            | 유선통신, 무선통신                                     |
    |----                                                                         ㅣ
    |  송수신자의 이동여부  | 고정통신, 이동통신                                     |
    |----
    | 신호형태             | 아날로그 통신, 디지털 통신                              |
    |----
    | 신호의 종류          | 전기통신, 광통신                                        | 
    |----
    | 이용대상             | 공중통신, 전용통신                                      | 
    |----
    | 정보의 표현 형태      | 음성통신, 데이터 통신, 화상통신, 영상통신, 멀티미디어 통신 | 
    |=====                                                                         ㅣ
### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

### Body text

Lorem ipsum dolor sit amet, test link adipiscing elit. **This is strong**. Nullam dignissim convallis est. Quisque aliquam.

![Smithsonian Image]({{ site.url }}/images/3953273590_704e3899d5_m.jpg)
{: .image-right}

*This is emphasized*. Donec faucibus. Nunc iaculis suscipit dui. 53 = 125. Water is H<sub>2</sub>O. Nam sit amet sem. Aliquam libero nisi, imperdiet at, tincidunt nec, gravida vehicula, nisl. The New York Times <cite>(That’s a citation)</cite>. <u>Underline</u>. Maecenas ornare tortor. Donec sed tellus eget sapien fringilla nonummy. Mauris a ante. Suspendisse quam sem, consequat at, commodo vitae, feugiat in, nunc. Morbi imperdiet augue quis tellus.

HTML and <abbr title="cascading stylesheets">CSS<abbr> are our tools. Mauris a ante. Suspendisse quam sem, consequat at, commodo vitae, feugiat in, nunc. Morbi imperdiet augue quis tellus. Praesent mattis, massa quis luctus fermentum, turpis mi volutpat justo, eu volutpat enim diam eget metus.

### Blockquotes

> Lorem ipsum dolor sit amet, test link adipiscing elit. Nullam dignissim convallis est. Quisque aliquam.

## List Types

### Ordered Lists

1. Item one
   1. sub item one
   2. sub item two
   3. sub item three
2. Item two

### Unordered Lists

* Item one
* Item two
* Item three

## Tables

| Header1 | Header2 | Header3 |
|:--------|:-------:|--------:|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|----
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|=====
| Foot1   | Foot2   | Foot3
{: rules="groups"}

## Code Snippets

Syntax highlighting via Rouge

```css
#container {
  float: left;
  margin: 0 -240px 0 0;
  width: 100%;
}
```

Non Pygments code example

    <div id="awesome">
        <p>This is great isn't it?</p>
    </div>

## Buttons

Make any link standout more when applying the `.btn` class.

```html
<a href="#" class="btn btn-success">Success Button</a>
```

<div markdown="0"><a href="#" class="btn">Primary Button</a></div>
<div markdown="0"><a href="#" class="btn btn-success">Success Button</a></div>
<div markdown="0"><a href="#" class="btn btn-warning">Warning Button</a></div>
<div markdown="0"><a href="#" class="btn btn-danger">Danger Button</a></div>
<div markdown="0"><a href="#" class="btn btn-info">Info Button</a></div>
