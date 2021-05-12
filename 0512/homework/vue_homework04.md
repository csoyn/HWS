# Vue_homework04

> Vuex



### 1. T/F

- Vue 프로젝트에서 상태 관리를 하기 위해서는 반드시 Vuex 를 설치해야 한다 **F**
- mutation 은 반드시 state 를 수정하기 위해서만 사용되어야 한다 **T**
- mutation 은 store.dispatch 로 action 은 store.commit 으로 호출할 수 있다 **F**
- state 는 data 와 동일하고 getters 는 computed 와 동일한 동작을 한다 **T**



### 2. Vuex 에서 action 과 mutation 의 역할과 두 함수의 차이를 서술하시오

* action : 데이터 fetch 와 처리, 가공, 비동기 작업
  * state를 직접 변경하지 않고, mutation에 정의된 메서드를 호출해서 변경
  * 첫번째 인자는 항상 context를 받음 / dispatch로 mutations의 메서드 호출
* mutation
  * state를 변경 / 첫 번재 인자로 항상 state를 받음 / commit을 통해 호출



