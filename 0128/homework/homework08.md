# Homework08



### 1. Circle 인스턴스 만들기

아래와 같은 Circle 클래스가 있을 때 , 반지름이 3 이고 x, y 좌표가 (2, 4)인 Circle 인스턴스를 만들어 넓이와 둘레를 출력하시오.

```python
class Circle:
    pi = 3.14
    x = 0
    y = 0
    r = 0

    def __init__(self, r, x, y):
        self.r = r
        self.x = x
        self.y = y

    def area(self):
        return self.pi * self.r *self.r
    def circumference(self):
        return 2 * self.pi *self.r
    def center(self):
        return (self.x , self.y)

cir = Circle(3,2,4)        
print(round(cir.area(), 2))
print(cir.circumference())
```



### 2.  Dog 과 Bird 는 Animal 이다
다음과 같이 Animal 클래스가 주어질 때 , 해당 클래스를 상속 받아 아래의 보기와 같이 동작하는 Dog 클래스와 Bird 클래스를 작성하시오.

```python

class Animal:

    def __init__(self, name):
        self.name = name

    def walk(self):
        print(f'{self.name}! 걷는다!')

    def eat(self):
        print(f'{self.name}! 먹는다!') 

class Dog(Animal):
    def __init__(self, name):
        self.name = name

    def walk(self):
        print(f'{self.name}! 달린다!')

    def bark(self):
        print(f'{self.name}! 짖는다!')    

class Bird(Animal):
    def __init__(self, name):
        self.name = name

    def fly(self):
        print(f'{self.name}! 푸드덕!')

dog =Dog('멍멍이')
dog.walk()     
dog.bark() 

bird = Bird('구구')
bird.walk()     
bird.eat()
bird.fly()
```

### 3. 오류의 종류

- ZeroDivisionError : 0으로 나누기연산을 했을 때
- NameError : 어떤 것이 정의되지 않았을 때
- TypeError : 타입이 맞지 않을 때, (정수형인데 문자열 메서드를 적용)
-  IndexError : 인덱스가 존재하지 않을 때
- KeyError : 딕셔너리의 key가 없을 떄
- ModuleNotFoundError : 모듈을 찾을 수 없을 때
- ImportError : 모듈의 import의 과정에서 에러