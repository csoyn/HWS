# Homework07

> 객체 지향 프로그래밍

### 1. Type Class

> Python 은 객체 지향 프로그래밍 언어이다 . Python 에서 기본적으로 정의되어 있는 클래스를 최소 5 가지 이상 작성하시오.

**Solution1**

리스트 / 딕셔너리 / 정수 / 소수 / 튜플



### 2. Magic Method

> 아래에 제시된 매직 메서드들이 각각 어떠한 역할을 하는지 간단하게 작성하시오.

**Solution2**

(1) `__init__` : 생성자 메서드로, 인스턴스가 생성될 때 호출되는 메서드. `(initialize)`

(2) `__del__` : 소멸자 메서드로, 인스턴스가 소멸될 때 호출되는 메서드` (delete)`

(3) `__str__` : 인스턴스를 `print`할 때, 보여줄 내용을 정의하는 메서드 `(string)`

(4) `__repr__` :  인스턴스를 문자열의 형태로 반환`(representation)`





### 3. Instance Method
> . sort() 와 같이 문자열 , 리스트 , 딕셔너리 등을 조작 할 때 사용하였던 것들은 클래스에 정의된 메서드들이었다 . 이처럼 문자열 , 리스트 , 딕셔너리 등을 조작하는 메서드를 최소 3 가지 이상 그 역할과 함께 작성하시오.

**Solution3**

(1) 문자열

	-  `strip()` :  공백제거나 특정문자를 제거하는 메서드
	-  `find()` :  찾고자 하는 문자의 첫 인덱스를 알려주는 메서드 / 없으면 -1
	-  `index()` : 찾고자 하는 문자의 첫 인덱스를 알려주는 메서드 / 없으면 에러
	-  `lower()` : 소문자로 바꿔주는 메서드
	-  `upper()` : 대문자로 바꿔주는 메서드
	-  `replace()` : 바꾸고자 하는 문자열을 특정 문자로 바꾸는 메서드

(2) 리스트

- `append()` : 값을 추가하는 메서드
- `extend()`:  값을 추가하는 메서드, 요소 하나씩 넣음
- `sort()` :  오름차순, 내림차순, 길이 순 등 으로 정렬할 수 있는 메서드
- `pop()`:  특정 위치에 있는 값을 삭제하고, 그 값을 반환하는 메서드.
- `count()`:  특정 값의 개수를 확인하는 메서드
- `insert()`:   특정 위치에 값을 추가하는 메서드

(3) 딕셔너리

- `items()` : 모든 key와 value를 pair 형태로 알려주는 메서드
- `keys()`: 모든 key를 알려주는 메서드
- `values() ` :모든 value를 알려주는 메서드
- `pop() ` : 특정 위치에 있는 값을 삭제하고, 그 값을 반환하는 메서드.
- `get()` : key에 접근할 수 있도록 하는 메서드



### 4. Module Import

> fibo.py 파일에 작성되어 있을 때 , 아래와 같은 형태로 함수를 실행 할 수 있도록 하는 import 문을 빈칸 ( a), ( b), ( 를 채워 넣어 완성하시오

```python
# fibo.py
def fibo_recursion(n):
    if n < 2:
        return n
	else:
        return fibo_recursion(n-1) + fibo_recursion(n-2)
        
```

```python
from a import b as c
recursion(4)
```

**Solution3**

- (a) : fibo

- (b) : fibo_recursion

- (c) : recursion