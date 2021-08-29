# 2021-08-24



Eclips Tern 플러그인 적용하기

Help - Install  New SoftWare

Work with에 h[ttp://oss.opensagres.fr](http://oss.opensagres.fr/)/tern.repository/1.2.0/ 추가 Add 이름에 tern 입력하고 설치

이클립스 재실행 후 원하는 프로젝트 우클릭 - configure - Convert to tern project선택





객체를 읽어오는 함수

```javascript
//1개 선택
document.getElementById("test1"); //id로 식별
document.querySelector("test1");
//여러개 선택
document.getElementsByTagName("a"); //태그 이름으로 식별
document.getElementsByClassName("test2"); // 클래스 이름으로 식별
document.querySelectorAll("test1");
```

주의할 점

getElementById

아래 둘은 id식별과 달리 배열에 값이 저장된다.

getElementsByTagName

getElementsByClassName

```javascript
var img = document.getElemmentsByTagName("태그명");
img.src = "/htmltest/images/파일명";
```





<h4>링크 DOM텍스트

이벤트란? 키보드나 마우스 동장이 영향을 미치는 것

*종류*

1. 마우스 이벤트 - 모든 html 가능
2. 키보드 이벤트 - input type 가능
3. 포커스 이벤트 - 모든 html 가능
4. 구조 변화 이벤트 - input type = checkbox, radio, select option
5. 터치 이벤트 - 기계 종속적

function action(){}

window.onload = action;

window로딩 완료되면 = 함수(자동)실행;

자바스크립트객체.onclick = function(){};

