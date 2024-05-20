# AJAX(Asynchronous Javascript And XML)
> 브라우저가 가지고 있는 XMLHttpRequest 객체를 이용해서 필요한 일부 페이지의 데이터만을 로드하는 기법

## AJAX 주요 기술
- XMLHttpRequest: 비동기 통신을 담당하는 자바스크립트 객체
- JavaScript: 객체 기반의 스크립트 프로그래밍 언어
- XML(eXtensible Markup Language): 특수한 목적을 갖는 마크업 언어[^markup]
[^markup]: 태그 등을 이용해 문서나 데이터의 구조를 명기하는 언어
- DOM(Document Object Model): XML 문서를 트리 구조 형태로 접근할 수 있게 하는 API
- XSLT(Extensible Stylesheet Language Transformation): XML문서를 다른 XML 문서로 변환하는데 사용하는 XML 기반 언어
- HTML(HyperText Markup Language): 인터넷 웹문서를 표현하는 표준화된 마크업 언어
- CSS(Cascading Style Sheets): 마크업 언어가 실제 표시되는 방법을 기술하는 언어

## AJAX 동작 원리
1. 사용자에 의한 요청 이벤트 발생
2. 이벤트 핸들러에 의한 자바스크립트 호출
3. 자바스크립트는 XMLHttpRequest 객체를 사용해 서버로 요청
4. 서버는 전달받은 XMLHttpRequest 객체를 가지고 AJAX 요청 처리
5. 서버는 처리한 결과를 웹브라우저에 전달
6. 웹페이지 일부만 갱신하는 자바스크립트 호출
7. 웹페이지 일부 갱신