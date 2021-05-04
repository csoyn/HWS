# JavaScripts HW04

> JavaScript 심화



### 1. T/F

- Event Loop는 Call Stack이 비워지면 Task Queue의 함수들을 Call Stack으로 할당하는 역할을 한다. **T**
- XMLHttpRequest(XHR)은 AJAX 요청을 생성하는 JavaScript API이다. XHR의 메서드 로 브라우저와 서버간의 네트워크 요청을 전송할 수 있다. **T**
- axios는 XHR(XMLHttpRequest)을 보내고 응답 결과를 Promise 객체로 반환해주는 라이브러리이다. **T**



### 2. 아래의 코드가 실행되었을 때 Web API, Task Queue, Call Stack 그리고 Event Loop에서 어떤 동작이 일어나는지 서술하시오 
```javascript
console.log('HELLO SSAFY!')

setTimeout(function () {
    console.log('I am from setTimeout')
}, 1000)

console.log('BYE SSAFT!')
```

**1)** `console.log('HELLO SSAFY!')` 가 먼저 `Call Stack` 에, `HELLO SSAFY` 가 출력되고, `Call Stack` 이 빔.

**2)** 빈 `Call Stack` 에 `setTimeout` 이 들어 왔다가, `Web API` 으로 보내고, `Web API`에 1초 머무른다.

**3)** `setTimeout` 이 `Web API` 으로 보내지고, 빈 `Call Stack`에 `console.log('BYE SSAFT!')`이 들어온다.

**4)** `BYE SSAFY`  출력되고,  `Call Stack`이 빔  +  `Web API`에 1초 머문 `setTimeout`이 `Task Queue`에 들어옴.

**5)** `Event Loop`로 인해  `Task Queue`에 있던  `setTimeout`이 `Call Stack`에 들어온다.

**6)**  `'I am from setTimeout'`이 출력되고, `Call Stack`이 비게 된다.



### 3. JS는 Event loop를 기반으로 하는 Concurrency model을 가지고 있다고 한다.  Concurrency 키워드의 특징을 작성하고, 이와 비슷한 키워드로 비교되는 Parallelism의 개념과 두 개념의 차이점을 서술 하시오.

**1)** `Concurrency model`  : Event Loop를 기반으로 하는 동시성 모델, 순서가 보장 되지 않는다. 

**2)** `Parallelism` : 병렬처리 (Promise)

**3)** `Promise` 콜백은 event queue에 배치되는 엄격한 순서로 호출 된다. 

- 각 콜백은 주어진 순서대로 하나씩 실행된다. (Chaining)

 