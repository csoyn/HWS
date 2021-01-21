# Homework01

> 데이터 & 제어문



## 1. Python 예약어

> python에서 사용할 수 없는 식별자(예약어)를 찾아 작성하시오.

**Solution 1**

1. 숫자로 시작하면 안되고, 특수문자 사용 불가능

2. 이미 있는 키워드(Fasle, True, and, as, if, else, elif, while, for, None 등 )

교재에서 가져온 키워드:

False, None, True, and, as, assert, async, await, break, class, continue, def, del, elif, else, except, finally, for, from, global, if, import, in, is, lambda, nonlocal, not, or, pass, raise, return, try, while, with, yield



## 2. 실수 비교

> python은 부동소수점 방식을 이용하여 실수(float)를 표현하는 과정에서, 나타내고자 하는 값과의 오차가 발생하여 원하는 대로 연산 또는 비교가 되지 않을 때가 있다. 이를 참고하여, 아래와 같은 두 실수 값을 올바르게 비교하기 위한 코드를 작성하시오.

```python
num1 = 0.1 * 3
num2 = 0.3
# 아래에 답안을 작성하시오.
```

먼저 두 개의 값을 비교해보면,

```python
num1 == num2
False
```

**Solution 2.1**

```python
num1_r = round(num1,2)
num1_r ==num2
True
```

**Solution 2.2**

```python
import sys
abs(num1-num2) <=sys.float_info.epsilon
True
```



## 3. 이스케이프 시퀀스

> (1) 줄 바꿈, (2) 탭, (3) 백슬래시를 의미하는 이스케이프 시퀀스를 작성하시오.

**Solution3**

```python
# 아래에 답안을 작성하시오.
\n 
\t
\\
```



## 4. String Interpolation

> “안녕, 철수야"를 string interpolation을 사용하여 출력하시오.

**Solution4**

name = '철수'

```python
print(f'"안녕, {name}야"')
print ('"안녕, {}야"'.format(name))
print('"안녕, %s야"' %name)
```



## 5. 형 변환

> 다음 중, 실행 시 오류가 발생하는 코드를 고르시오.

```python
str(1) # (1)
int('30') # (2)
int(5) # (3)
bool('50') # (4)
int('3.5') # (5)
```

**Solution5**

```python
# 아래에 답안을 작성하시오.
# (5번) 3.5가 실수형이 아닌 문자열이므로 정수로 변환 불가 
# int(3.5) 얘는 가능
```



## 6. 네모 출력

> 두 개의 정수 n과 m이 주어졌을 때, 가로의 길이가 n, 세로의 길이가 m인 직사각형 형태를 별(`*`) 문자를 이용하여 출력하시오. 단, 반복문은 사용할 수 없다.

**Solution6**

```python
n = 5
m = 9

a = '*'*n
print(f''' 
{a}
{a}
{a}
{a}
{a}
{a}
{a}
{a}
{a}
''')
# 어...이걸 줄이면 
print(( a + '\n') * m)
```



## 7. 이스케이프 시퀀스 응용

> `print()` 함수를 한 번만 사용하여 다음 문장을 출력하시오.

```
"파일은 c:\Windows\Users\내문서\Python에 저장이 되었습니다."
나는 생각했다. 'cd를 써서 git bash로 들어가 봐야지.'
```

**Solution7**

```python
# 아래에 답안을 작성하시오.
print('''
"파일은 c: \\Windows\\Users\\내문서\\Python에 저장이 되었습니다."
나는 생각했다. 'cd를 써서 git bash로 들어가 봐야지.'
''')
```

## 8. 근의 공식

> 다음은 이차 방정식의 근을 찾는 수식이다. 이를 파이썬 코드로 작성하시오.

![image](hws0118.assets/87770068-7774a880-c859-11ea-8433-7be4ad1fa4e4.png)

**Solution8**

a, b, c가 실수로 가정했을 때
$$
a x^2 +b x +c = 0
$$
의 실근을 구하는 근의 공식(complex형은 비교연산자 부등호를 쓰지 못하는 것으로 알고 있어서...)

```python
a, b, c = map(float, input("실수 세 개를 공백으로 구분하여 입력").split())

D = (b**2)-(4*a*c)
if D < 0 :
    print('서로 다른 두 허근을 가진다.')
elif D == 0:
    print('중근을 가지고 그 근은 아래와 같다')
    x = (-b) / (2*a)
    print(x)
else:
    print('서로 다른 두 실근은 아래와 같다.')
    x_1 = (-b + (D**0.5)) / (2*a)
    x_2 = (-b - (D**0.5)) / (2*a)
    print(x_1,x_2)
```

