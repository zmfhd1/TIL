# 2021-08-25(금)





img => src, width, height

a => href

input => type, value, size, maxlength





### jquery

1. java script - 변수 연산자 함수 객체 dom이벤트
2. dom + 이벤트



일단 제이쿼리를 사용하려면 제이쿼리 라이브러리를 추가해야한다.

jquery 홈페이지에서 파일을 다운받아 이클립스 프로젝트에 추가한다.



이클립스 템플릿 수정

이클립스에서  특정 파일을 새롭게 만들 때 기본적으로 적혀있는 구문을 수정할 수 있다.

Window - preference - web - editor - templates - html5 - edit 하여 원하는 문구 삽입



1. jquery와 javascript 비교

   ```javascript
   $(document).ready(function(){
       $("h1").css("color","red");
   }
   //javascript에 비해 jquery는 간단한 구문을 사용해도 알아서 처리해준다
   ==================================================================            
   window.onload = function(){
       document.getElementsByTagName("h1")[0].style.color = "red";
   }
   ```



2. jquery 실습

   ```javascript
   <script src="jquery-3.2.1.min.js"></script>
   <script>
   $(document).ready(function() {
   	//$('h1').css("color", "blue"); // h1태그 속성 변경
   	//$("#second").css("color", "blue"); //id-second 속성 변경
   	//$(".red").css("background-color", "#ff0000"); //class=red 태그 속성 변경
   	//$('h1>a').css('text-decoration', 'none'); //h1태그 내부에있는 a태그 속성 변경
   	//$("h1,td").css("background-color", "yellow"); //h1태그와 td 태그 속성 변경
   	//$("h1.red").css("background-color", "yellow"); //class=red인 h1태그 속성 변경
   	//$("input[type=text]").css("background-color", "yellow"); //input type=text 태그 속성 변경
   	//$("input:password").css("background-color", "yellow"); //input type=password 태그 속성 변경
   	//$("input:button").css("background-color", "yellow"); //input type=button 태그 속성 변경
   	//$("input:button, button").css("background-color", "yellow"); //input type=button, 태그가 button인 2개의 태그 속성 변경
   	//$("th").css("background-color", "pink"); //th태그 배경 변경
   	//$("tr:first").css("background-color", "orange"); //첫번째 tr태그 배경 변경
   	//$("tr:last").css("background-color", "orange"); //마지막 tr태그 배경 변경
   	//index는 0부터 시작이기때문에 우리가 생각하는 홀,짝을 다르게 인식한다
   	//$("tr:even").css("background-color", "aqua"); //홀수 tr태그 배경 변경
   	//$("tr:odd").css("background-color", "orange"); //짝수 tr태그 배경 변경
   	//$("tr:gt(2)").css("background-color", "orange");//4번째 tr부터 나머지 모든 tr태그 변경 gt => greater than()=뭐보다 클때 
   	//$("tr:gt(2), tr:eq(2)").css("background-color", "orange");//3번째 tr부터 나머지 모든 tr태그 변경 gt => greater than()=뭐보다 클때 
   	//$("tr:lt(2)").css("background-color", "orange");//3번째 이하 tr태그 변경
   	//$("tr:nth-child(3n)").css("background-color", "orange");//tr인덱스 3의 배수
   </script>
   ```

   

3. jquery 함수

   * css (스타일)

   ```javascript
   css("속성명", "값"); --> setter
   css("속성명"); --> getter
   ```

   * attr (속성)

   ```javascript
   attr("태그 속성명", "값"); --> setter
   attr("태그 속성명"); --> getter
   removeAttr("태그 속성명"); --> 삭제
   ```

   - html (문서 객체 내부의 html태그 조작)

   ```javascript
   innerHTML 변수같은 역할
   
   html() => getter
   html("") => setter
   
   html 함수는 지정한 태그 내에서 존재했던 태그들을 모두 없애고 다시 새롭게 작성하는 방법을 말한다.
   ```

   - append(태그 내부 컨텐츠 출력)

   ```javascript
   append 함수는 지정한 태그 내에서 존재했던 태그들을 그대로 놔둔채 태그를 추가하는 방법이다.
   ```

   - text (문서 객체 내부의 글자 조작)

   ```javascript
   text() => getter
   text("") => setter
   ```

   - 

   ```javascript
   
   ```

   - empty() / remove()

   ```javascript
   $("#contents").empty; //자식요소를 제거
   $("#contents").remove; //나 자신 제거
   ```

   - addClass / removeClass / toggleCalss

   ```javascript
   클래스명이 있어야 도움이된다.
   ```

   - val

   ```javascript
   val() => getter
   val("") => setter
   ```

   - on (이벤트 연결) / off (이벤트 제거) / one(최초 한번만 이벤트 실행)

   ```javascript
   $('').click(funcion(e){});
   $('div').on('click', function(e){})
   
   on함수와 one함수의 차이 => on함수는 off해줄때까지 계속되지만, one함수는 최초 한번만한다.
   ```

   - hide /show

   ```javascript
   ```

   - aa

   ```javascript
   
   ```

   

