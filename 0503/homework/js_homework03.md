# JavaScript HW3

> Asynchronous JavaScript



### 1. T/F

- JavaScript는 single threaded 언어로 한번에 한가지 일 밖에 처리하지 못한다.    **T**
  - 스레드는 한 번에 하나의 작업만 수행할 수 있다.

- setTimeout은 브라우저의 Web API를 사용하는 함수로, Web API에서 동작이 완료 되면 Call Stack에 바로 할당된다.      **F** (web API -> Task Queue -> event loop 가 Call Stack)
- Prmoise 객체를 생성할 때 인자로 받는 callback 함수인 resolve와 reject는 비동기 처리가 성공/실패 했을 경우 어떠한 값을 전달할지 결정한다. **T**
- Promise 객체의 .then 메서드는 오류 없이 resolve 되었을 때 실행되는 함수이며, .catch 메서드는 도중에 오류가 발생하여 reject 되었을 때 실행되는 함수이다. **T**
  - Promise 객체(결과)가 다음으로 넘어감.



### 2. JavaScript에서 동기와 비동기 함수의 차이점을 서술하시오

**동기식** : 순차적, 직렬적으로 Task를 수행한다. 함수가 끝날 때 까지 다음 동작이 이루어지지 않는다.(blocking)

**비동기식** : 병렬적으로  Task를 수행한다. 함수가 끝날 때까지 기다리지 않고 다음 동작이 이루어짐(non-blocking)



### 3. 다음은 axios를 사용하여 API 서버로 요청을 보내고, 응답 데이터를 출력하는 코드이다. (a), (b), (c)에 들어갈 코드를 작성하시오.

```javascript
axios./*(a)*/('https://api.example.com/data')
	./*(b)*/function (response) {
    console.log(/*(c)*/)
})
```

**(a)** : get

**(b)** : then

**(c)** : response.data