# Django hw02

> Django Template and View
> Static web and Dynamic web

### 1. MTV

Django는 MTV 디자인 패턴으로 이루어진 Web Framework 이다 . 여기서 MTV 는 무엇의
약자이며 각각 MVC 디자인 패턴과 어떻게 매칭이 되며 각 키워드가 django 에서 하는역할을
간략히 서술하시오.

**답**)

1. Model : 데이터베이스에 저장되는 **데이터**를 의미.
   + 장고는 sql을 몰라도 db작업을 가능하게 하는ORM(object-relational mapping)을 제공.
2. Template : **사용자에게 보여지는 부분** html파일이 담당?하고 있음. 
3. View :  전달받은 데이터들을 해당 **어플리케이션의 로직으로 가공**하여, 그 결과를 템플릿에 보내준다. View에서 **함수**를 작성.



### 2. URL

__(a)__는 Django 에서 URL 자체를 변수처럼 사용해서 동적으로 주소를 만드는 것을
의미한다 . 

**답** ) Variable Routing



### 3. Django template path

Django 프로젝트는 render 할 template 파일들을 찾을 때 , 기본적으로 settings.py 에
등록된 각 앱 폴더 안의 __a)__ 폴더 내부를 탐색한다 .

**답**) templates/ app 이름 폴더 ????



### 4. Static web and Dynamic web
Static web page 와 Dynamic web page 의 특징을 간단하게 서술하시오

**답**)

- Static web page(정적 웹 페이지)

  서버에 **미리 저장되어있는 파일** 이 그대로 정달되는 웹 페이지 / 서버의 데이터가 변경되지 않는 한 고정된 웹 페이지를 보게 됨

- Dynamic web page(동적 웹 페이지)

  서버에 있는 데이터들을 스크립트에 의해 가공처리 후 생성되어 전달되는 웹 페이지 

  / 서버는 사용자의 **요청(Request)**에 따라 데이터를 가공한 후 웹 페이지를 보냄

  / 시간, 요청, 상황에 따라 웹 페이지가 달라짐.