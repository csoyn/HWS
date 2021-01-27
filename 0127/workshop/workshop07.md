# Workshop07

> 객체 지향 프로그래밍



## Problem

Faker는 개발시 활용할 수 있는 가상의 데이터를 생성해주는 파이썬 패키지이다.

워크샵에 등장하는 코드는 모두 Github( https://github.com/joke2k/faker ) 문서의 예제이다
지금까지 배운 파이썬 개념을 활용하여 해석 하시오.

### 1. pip

$ pip install faker

**Solution1**

(1)  무엇을 위한 명령 :  faker 패키지설치를 위한 명령어

(2) 실행은 어디에서  : 터미널?창



### 2.  Basic Usages
https://github.com/joke2k/faker#basic-usage
Faker는 다양한 메서드를 통해 임의의 결과값을 반환해준다. 임의의 영문 이름을 반환하는 아래 코드에서 라인별 의미를 주석을 참고하여 작성하시오.

**Solution2**

```python
from faker import Faker  # 1. fakek모듈에서 Faker를 가져오는 코드

fake = Faker()  # 2. Faker 클래스,(에 속하는) fake는 인스턴스(객체) 생성

fake.name()    #  3. name( )은 fake의 메서드 이다.
```



### 3. Localization

(https://github.com/joke2k/faker#localization) Faker는 다양한 언어의 Locale을 지원한다.

**Solution3**

```python
class Faker():
    def __init__(self,name):
        pass
```



### 4. Seeding the Generator

https://github.com/joke2k/faker#seeding-the-generator

컴퓨터프로그래밍에서 임의의 값을 반환하는 경우 난수 생성 등 시드라는 개념이 있다. 시드를
설정하게 되면 동일한 순서로 난수를 발생시킬 수 있어 일반적으로 디버깅을 위하여 활용 된다.

**Solution4**

```python
fake = Faker('ko_KR')  	
Faker.seed(4321)
print(fake.name())		# seed를 정하고, seed넘버와 같이 컴파일하면 동일한 결과가 나옴.
```

```python
fake2 = Faker('ko_KR')
print(fake2.name())		# seed 없이 반복적으로 컴파일하면, 다른 이름이 출력 됨.
```

-> 같은 패턴의 난수를 생성하기 위한 메서드 (씨앗(seed)이 똑같으면 싹도 똑같음)