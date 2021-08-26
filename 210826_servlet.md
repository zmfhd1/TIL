# 2021-08-26(목)



웹클라이언트 기술 - 브라우저가 해석하고 실행

| 웹클라이언트 기술 - 브라우저가 해석하고 실행 | 웹 서버 기술 - 브라우저의 요청을 받아 실행 |
| -------------------------------------------- | ------------------------------------------ |
| html - 컨텐츠(slient side markup program)    | servlet                                    |
| css - 스타일                                 | jsp                                        |
| java script - 동작                           | spring                                     |
| jquery                                       | mybatis                                    |
| 하지만 이런것들은 한정적이다 -> DB이용 기술x |                                            |
|                                              |                                            |





---



### 서블릿이란?

서블릿은 서버쪽에서 실행되면서 클라이언트의 요청에  따라 동적으로 서비스를 제공하는 자바클래스이다. (서버에서 작동하는 자바)



서블릿의 생명주기 메소드

```java
//	서버 종료시, 서블릿 코드 수정 - 재컴파일 시, 이전 서블릿 객체 삭제시
	@Override
	public void destroy() {
		System.out.println("destroy 메소드 호출");
	}
	
//	서버시작 최초 한번 실행
//	저장-자동 컴파일- (이전 서블릿 객체 사라짐 - destroy 실행) - 
	@Override
	public void init() throws ServletException {
		System.out.println("init 메소드 호출");
	}
	
//	호출(요청)할 때마다 여러번 실행
	protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		System.out.println("doGet 메소드 호출");
	}

```







---



### 서블릿 매핑 자바 파일 정의한 후에 실행 2가지 방법

1. WebServlet
   - @WebServlet을 사용



2. Web.xml

   ```xml
     <servlet>
     <servlet-name>t</servlet-name>
     <servlet-class>test.TestServlet</servlet-class>
     </servlet>
     
     <servlet-mapping>
     <servlet-name>t</servlet-name>
     <url-pattern>/test</url-pattern>
     </servlet-mapping>
   ```









---



### 서블릿 실행과정

1. 서블릿 객체 메모리에 생성
2. 생성자 실행
3.  init 실행
4. doGet 실행





http프로토콜 규칙

1. 사용자가 전송한 데이터 : url?파라미터명=값&...
2. 클라이언트에서 서버로 데이터 전송 (폼 방식)
   - 기본 방식은 get : url 뒤에 사용자가 전송한 데이터가 모두 표시된다.
   - post : url에 데이터가 보이지 않고 전송된다.