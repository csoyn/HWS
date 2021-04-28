# Homework 18

> JavaScript
> DOM(Document Object Model) 조작



### 1. T / F

- document.createElement 메서드를 통해 HTML 요소를 생성할 수 있다. **T**
- EventTarget .addEventListener (type, listener)에서 listener 에 작성되는 콜백 함수의 첫번째 매개변수는 발생한 이벤트를 설명하는 Event 에 기반한 객체이다. **F**
- event .preventDefault 메서드를 통해 이벤트 동작을 취소할 수 있다 **T**
- 부모 노드에서 자식 노드를 추가하는 유일한 방법은 append 메서드 뿐이다 **F**



### 2. click, mouseover, mouseout, keydown, keyup load, scroll, change, input

위 Event 들이 각각 어떤 시점에 발생하는지 다음 MDN 문서를 참고하여 간단하게 작성하시오.

https://developer.mozilla.org/ko/docs/Web/Events

- click : 모든 버튼 - 엘리먼트에서 눌렸다가 놓였을 때 (마우스)

- mouseover - 등록된 엘리먼트나 그 자식 엘리먼트의 위로 이동했을 때 (마우스)

- mouseout  -  등록된 엘리먼트 또는 그 자식 엘리먼트의 밖으로 이동했을 때 (마우스)

- keydown    -  키가 눌렸을 때 (키보드)

- keyup         -  키 누름이 해제될 때 (키보드)

- load            -  리소스와 그 의존 리소스의 로딩이 끝났을 때 (리소스 이벤트)

- scroll          -  다큐먼트 뷰나 엘리먼트가 스크롤되었을 때 (뷰 이벤트)

- change      -   `<input>` `<select>` `<textarea>` 요소가 user에 의해 변경이 있을 때,

  ​	                    input과 달리 각 변경마다 반드시 발생하진 X  (value 저장소이벤트)

- input         -  `<input>` `<select>` `<textarea>` 에서 user에 의해 변경 (값 변경 이벤트)



### 3. 버튼을 클릭했을 때 콘솔창을 통해 메시지를 확인하는 코드이다

<img src="homework18.assets/image-20210428180731117.png" alt="image-20210428180731117" style="zoom:80%;" />

**(a)** : querySelector

**(b)** : addEventListener

**(c)** : click