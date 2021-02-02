# Homework02

> HTML layout & CSS Selector



### 1. Semantic Tag

header / footer / section 



### 2. input Tag

아래 이미지와 같이 로그인 Form 을 생성하는 HTML 코드를 작성하시오 .
단 , USERNAME 글자를 클릭하면 아이디를 입력하는 input 에 PWD 글자를 클릭하면 비밀번호를 입력하는 input 에 focusing 되도록 하시오.

![image-20210202155214340](web_02_homework.assets/image-20210202155214340.png)

답) body 부분만 & 결과창

```html
<section>
    <div>
      <label> USERNAME:<input type="text" autofocus placeholder="아이디를 입력 해 주세요."></label><br>
      <label> PWD : <input type="password" autofocus></label> <button> 로그인</button>
    </div>
  </section>
```

![image-20210202161043502](web_02_homework.assets/image-20210202161043502.png)



### 3.크기 단위

크기 단위 em은 요소에 지정된 상속된 사이즈나 기본 사이즈에 대해 상대적인 사이즈를 설정한다. 즉, 상속의 영향으로 사이즈가 의도치 않게 변경될 수 있는데 이를 예방하기 위해 HTML 최상위 요소의 사이즈를 기준으로 삼는 크기 단위는 무엇인가?

답) vw , vh (viewport width viewport height ) / 부모요소를 기준으로 %한다.



### 4. 선택자

```html
/*자손*/
div p {
color : crisom;
}
/*자식*/
div > p {
color : crisom;
}
```



답) 자손결합자는 모든 p 자손들을 가르키고, 

자식결합자 >를 사용하면 자식들 중에서 p인 자식들만 가르킨다.

