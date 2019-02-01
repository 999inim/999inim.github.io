---
title:  "개발상식 - 기본교육"
last_modified_at: 2019-02-01T16:01:04-04:00
categories: 
  - Study
tags:
  - update
toc: true
toc_label: "Getting Started"
---


### 프로그래밍 기본

#### XML, DrawingML, WordML
* XML이란?

텍스트 파일의 사용 용이성과 바이너리 파일의 풍부한 메타 정보 추가 능력을 결합한 이상적인 파일형식이 필요했다.
초기에는 SGML을 사용하였으나 매우 복잡하였고 좀 더 표준화되어 XMLL이 등장하였다. 범용적으로 데이터를 마크업하기 위해서 만들어졌다.

이를 통해서 문서를 구조화하고 데이터 교환을 쉽게한다.

특히나, 데이터를 위한 명세와 데이터를 짝짓고 임의로 제약(DTD)을 가할 수 있다는 특징이 있다.

* XML Parser
- 마크업 부분과 데이터부분을 분리하여 정보를 추출하고 다른프로그램이 사용가능한 형태로 만들어주는 프로그램이다.

분리하는 기준으로 CDATA와 PCDATA가 있다.
- CDATA는 Parser가 분석하지 않아야하는 속상값이나 블록등을 말한다.
- PCDATA는 Parsed Character Data의 약자로 Xml요소 사이의 데이터를 말한다. 


* Well-formed Document
xml의 구조가 제약조건에 맞는 문서인경우를 말한다.

> 처음에는 단순히 메모장에서 텍스트를 읽는 것처럼 단순한 문서구조만으로도 워드프로세서들이 다양한 편집이 가능한 것으로 생각했는데 내부적으로는 복잡한 구조를 파싱해서 보여주는 점이 신기했다.

### 웹브라우저와 렌더링엔진

* 웹(World Wide Web)
인터넷 연결을 통하여 정보를 공유할 수 있는 정보공간

* 웹브라우저
웹을 시각적으로 볼 수 있게끔 하는 응용프로그램

- 렌더링엔진
웹 컨텐츠를 레이아웃 정보에 맞게 보여줌. 각 회사마다 고유의 엔진이 있다.

- 렌더링 과정
HTML, DOM, CSS, SVG, Canvas를 각각의 Parser를 이용해 Tree구조의 Object로 만든 후 그린다.

- Tree 구조
DOM : html의 각 요소 하나하나를 객체화하여 tree구조를 띰.

CSSOM : DOM타입의 요소에 속성값을 붙임.

> 브라우저 자체를 인터넷으로 생각하는 경우가 있는데 웹에 있는 데이터들이 어떤 방식으로 렌더링되어 브라우저에 표현되는지에 대해 간략히 배울 수 있었다.


### OSS License

주요 의무사항
* 저작권, 개발자 및 기여자 정보 표시
* 코드 수정한 경우 수정한 정보 표시
* 라이선스 정보 제공
* 동일한 라이선스로 재배포(CopyLeft)
* 소스코드 제공


- 주요 오픈소스SW 라이선스 비교

|                | 무료 이용가능 | 배포 허용가능 | 소스코드 취득가능 | 소스코드 수정가능 | 2차적 저작물 재공개 의무 | 독점SW와 결합가능 |
|----------------|---------------|---------------|-------------------|-------------------|--------------------------|-------------------|
| GPL            |       o       |       o       |         o         |         o         |             o            |         x         |
| LGPL           |       o       |       o       |         o         |         o         |             o            |         o         |
| MPL            |       o       |       o       |         o         |         o         |             o            |         o         |
| BSD license    |       o       |       o       |         o         |         o         |             x            |         o         |
| Apache license |       o       |       o       |         o         |         o         |             x            |         o         |

### 다국어

* 다국어 개념
(internationalization/ localization / globalization)

- internationalization
개발 프로세스에서 다른 국가나 문화에 대한 소프트웨어 적용.
리소스와 개발코드의 분리하는 과정. 즉, 조금 더 개발 관련한 프로세스.

ex)
언어적 제약상황
Shaping Engine - 아랍어, Input Method Editor - 중국어

운영체제 인코딩
개발시스템에서 유니코드를 사용할 수 있는지 여부.

하드웨어
아시아권 글자(중국어)를 표시하는데 필요한 메모리, 메모리가 충분한지 여부.

하드코딩
자동 번역이 안되는 데이터를 사용하는 부분.
문자열, 아이콘에 이미지텍스트 경우 언어적 이슈가 생긴다.

- localization
다국어 "번역", Translation 뿐만이 아님.
현지 환경에 대한 테스트(언어적 특징등)

ex)
렌더링, 단위(Measurement, Date, Time, Address), Symbol(적십자 마크)

- globalization
Sales & Marketing

* Testing
현지화 완성도를 보장

- Linguistic Testing
문법, 스펠링, 구두점, 애매한 번역, 오번역.
- Functional Testing
- Cosmetic Testing
- Internationalization Testing
텍스트가 밖으로 나가거나, 번역이 안되는 증상, 소스코드가 드러나는등
표준화된 검증 절차(I18N)를 통해 해결.

