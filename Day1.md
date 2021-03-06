# Day 1


CPU의 레지스터에는 데이터를 처리하는 방식이 제조사마다 다르게 하드코딩 되어있다.

따라서 C언어는 CPU의 제품 종류, 세대가 달라졌을때 컴파일된 코드의 결과가 달라질수 있다.

그래서 우리는 C언어가 OS, H/W에 종속되어있다고 표현한다.   

이런 문제를 해결하기 위해 나온언어가 JAVA이다.   
JAVA는 JVM(JAVA Virtual Machine)을 통해 이 문제를 해결했다.

JVM을 사용하게되면서 JAVA는 플랫폼, OS에게 독립되었다.
(Write Once, Run Anywhere)

## 일반 프로그램과 JAVA 프로그램의 구조
___
![일반프로그램과 JAVA프로그램의 구조](https://yoojh9.github.io/images/jvm.png)
___

이러한 JAVA의 장점 때문에 WEB에서 JAVA가 널리쓰이게 된것이다.


|WEB 구조|
|:--:|
|Context|
|WAS|
|JVM|
|OS|
|Sever Infra|

WAS위에 여러 Context가 존재하게 되고 이것을 기반으로 url 주소가 정해지는것이다.

## 주소의형식
http://192.168.20.66:9999/Test/hello/hi.html


* 프로토콜 : http (WEB Service)
* 도메인주소 (IP) : localhost (자기 자신)
* 포트번호 : 9999 (Apache Tomcat 서버에서 정해놓은 포트)
* 컨텍스트 Path(경로) : /Test
&파일(자원, Resource)의 위치 : /hello/hi.html


# 과제
1. 이클립스 설치 및 설정 공부
https://ooz.co.kr/190?category=818548
 --> 단 최신의 이클립스 설치를 위해 아래의 링크 버전을 다운로드 받으세요
       https://www.eclipse.org/downloads/download.php?file=/technology/epp/downloads/release/2021-03/R/eclipse-jee-2021-03-R-win32-x86_64.zip

2. 톰캣 설치하기
https://ooz.co.kr/243?category=818548

3. 이클립스 기반 웹 프로젝트 생성해 보기
https://ooz.co.kr/262?category=818548

4. hello jsp 생성해 보기
https://ooz.co.kr/263?category=818548

# 질문

WAS와 Web Server의 차이
   
웹서버
작성된 HTML페이지 등을 네트워크망에 종속되지않고, 웹서비스를 할수 있도록 하는 어플리케이션

WAS(Web Application Server)
웹서버 + 웹컨테이너
인터넷 상에서 http를 통해 사용자 텀퓨터나 장치에 애플리케이션을 수행해주는 미들웨어(소프트웨어 엔진)이다.
웹상에 사용하는 컴포넌트를 올려놓고 사용하게되는 서버이다.

웹컨테이너(서블릿 컨테이너)
JSP와 Servlet을 실행시킬 수 있는 SW
JSP, Servlet 구동환경 제공 (동정 DATA처리)

웹서버에서 JSP를 요청하면 톰캣에서 JSP파일을 서블릿으로 변환하여 컴파일 수행
서블릿 수행결과를 웹서버에 전달한다.

Web Container의 유무로 WEB과 WAS를 나눌수 있다.

WEB서버는 HTML 문서같은 정적 컨테츠 처리(HTTP 프로토콜을 통해 읽힐수 있는 문서)

WAS서버는 asp,php,jsp 등 개발 언어를 읽고 처리하여 동적컨테츠, 웹 응용프로그램 서비스를 처리하는것이다.

apache는 웹서버
tomcat은 WAS

[출처](https://helloworld-88.tistory.com/71)

# 용어정리

## CPU(Central Processing unit)

CPU는 사람의 두뇌와 같이 컴퓨터 시스템에 부착된 모든 장치의 동작을 제어하고 명령을 실행하는 장치입니다. 중앙 처리장치는 제어장치, 연산장치, 레지스터 그리고 이들을 연결하여 데이터를 전달하는 버스로 구성되어 있습니다.

## Register(레지스터)
레지스터(Register)는 CPU 내부에서 처리할 명령어나 연산의 중간 결과값 등을 일시적으로 기억하는 임시 기억장소입니다.

## Servlet
JAVA를 이용하여 웹페이즈를 동적으로 생성하는 서버측 프로그램
흔히 CGI(Common Gateway Interface)라고들 하는데 CGI는 사용자의 입력을 받아서 동적인 HTML문서로 만드는것
Servlet이란 JAVA로 구현한 CGI

## JSP
jsp는 html문서에 java언어를 삽인한것
Sevlet이란 java언어로 이루어진 웹프로그래밍 문서
