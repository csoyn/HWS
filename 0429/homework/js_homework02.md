# JavaScript_hw2

> JavaScript



### 1. T/F

- let const 키워드로 선언한 변수와 var 키워드로 선언한 변수의 유일한 차이점은 변수의 유효범위이다 **F** (재선언 가능, 함수 스코프)
- 값이 없음 을 표현하는 값으로 null 과 undefined 두 종류가 있으며 둘 다 typeof 연산자에서 undefined 가 반환된다 **F** (null의 typeof 결과는 object)
- for in 문을 통해 배열의 각 요소를 순회할 수 있다 **T** (순회는 할 수 있음)
- `==`연산자는 두 변수의 값과 타입이 같은지 비교하고 같다면 true 아니면 false를 반환한다 **T**
- JavaScript 에서 함수는 변수에 할당 , 인자로 전달할 수 있으나 함수의 결과값으로 반환할 수는 없다 **F**



### 2. 다음의 Array Helper Method 의 동작을 간략히 서술하시오.

  **공통 : 배열의 각 요소에 대해 콜백 함수를 한 번씩 실행**

- **map** :  콜백 함수의 반환 값을 요소로 하는 새로운 배열 반환/ 기존 배열 전체를 다른 형태로 바꿀 때 유용
- **filter** : 콜백 함수의 반환 값이 참인 요소들만 모아 새로운 배열을 반환 / 기존배열을 필터링할 때 유용
- **find** : 콜백 함수의 반환 값이 참이면 해당 요소를 반환 / 찾는 값이 배열에 없으면 undefined 반환
- **every** : 배열의 모든 요소가 주어진 판별 함수를 통과하면 참을 반환 / 모든 요소가 통과하지 못하면 거짓 반환
- **some** : 배열의 요소 중 하나라도 주어진 판별 함수를 통과하면 참을 반환 / 모든 요소가 통과하지 못하면 거짓
- **reduce** : 콜백 함수의 반환 값들을 하나의 값 acc 에 누적 후 반환



### 3. map 함수를 사용하여 모든 아이템에 3 제곱을 한 새로운 배열을 만드는 코드를 작성

```javascript
const nums = [1,2,3,4]
const cubic = nums.map((num) =>{
    return num**3
})
// (4) [1, 8, 27, 64]
```
