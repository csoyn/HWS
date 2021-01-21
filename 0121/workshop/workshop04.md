# Workshop04

> 함수



### Problem

아스키코드는 미국 ANSI 에서 표준화한 정보교환용 7 비트 부호체계이다 . 아스키 코드는 총 128 가지의 문자를 나타낼 수 있으며 각각의 문자를 나타내는 숫자값이 존재한다 .



### 1. 숫자의 의미

정수로 이루어진 list 를 전달 받아 , 각 정수에 대응되는 아스키 문자를 이어붙인 문자열을 반환하는 get_secret_word 함수를 작성하시오 . 단 , list 는 65 이상 90 이하 그리고 97 이상 122 이하의 정수로만 구성되어 있다.

**Solution1**

```python
def get_secret_word(numbers):
    for num in numbers:
        result = chr(num)
        print(result, end='')  
get_secret_word ([83, 115, 65, 102, 89])
```





### 2. 내 이름은 몇일까

문자열을 전달 받아 해당 문자열의 각 문자에 대응되는 아스키 숫자들의 합을 반환하는 get_secret_number 함수를 작성하시오 . 단 , 문자열은 A~Z, a~z 로만 구성되어 있다.

**Solution2**

```python
name = 'seoyun'
def get_secret_number(words):
    total=0
    for word in words:
        total += ord(word)
    return total
get_secret_number(name)
get_secret_number('tom')
```



### 3. 강한 이름
문자열 2 개를 전달 받아 두 문자열의 각 문자에 대응되는 아스키 숫자들의 합을 비교하여 더 큰 합을 가진 문자열을 반환하는 get_strong_word 함수를 작성하시오.

```python
def get_secret_number(name1, name2):
    tot1= 0
    tot2 = 0
    for n1 in name1:
        tot1 += ord(n1)
    for n2 in name2:
        tot2 += ord(n2)
    if tot1 > tot2:
        return name1
    else:
        return name2
    
get_secret_number('z', 'a')
get_secret_number('tom', 'john')    
```















