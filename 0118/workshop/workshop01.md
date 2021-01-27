# Workshop

> 데이터 & 제어문

## 1. 세로로 출력하기

> 자연수 number를 입력 받아, 1부터 number까지의 수를 세로로 한줄씩 출력하시오.

---
**Solution1.1**

```python
number = int(input())
# 아래에 코드를 작성하시오.
A = 0
while A < number : # A가 number에 도달할 때까지
    A = A +1 # A에 1씩 더함
    print(A) 
```



**Solution1.2**

```python
number = int(input())
for i in range(1,number+1):
    print(i)
```



## 2. 가로로 출력하기
자연수 number 를 입력 받아 , 1 부터 number 까지의 수를 가로로 한칸씩 띄어 출력하시오

> 0121 추가

**Solution2**

```python
number = int(input())
for i in range(1, number+1):
    print(i, end =' ')
```



## 3. 거꾸로 세로로 출력하기

> 자연수 number를 입력 받아, number부터 1까지의 수를 세로로 한줄씩 출력하시오.

**Solution3.1**

```python
number = int(input())

# 아래에 코드를 작성하시오.
A = number
while A > 0: # A가 0에 도달할 때까지
    A = A - 1 # A에 -1씩 
    print(A)
```

**Solution3.2**

```python
number = int(input())
for i in range(number,0,-1):
    print(i)
```





## 4. 거꾸로 출력해 보아요 

자연수 number 를 입력 받아 , number 부터 0 까지의 수를 가로로 한칸씩 띄어 출력하시오.

> 0121 추가

```python
number = int(input())
for i in range(number,-1,-1):
    print(i, end =' ')
```



## 3. N줄 덧셈 (SWEA #2025)

> 입력으로 자연수 number가 주어질 때, 1부터 주어진 자연수 number까지를 모두 더한 값을 출력하시오. 단, 주어지는 숫자는 10000을 넘지 않는다. 예를 들어, 주어진 숫자가 10일 경우 1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9 + 10 = 55이므로, 출력해야 할 값은 55이다.

---
**Solution3.1**

```python
number = int(input())

# 아래에 코드를 작성하시오.
A = 0 # 더할 수 
tot = 0 # 합
while A <= number: # A가 number와 같아질 때까지
    tot = tot + A # tot에 A를 더함,
    A = A +1 # A를 1씩 증가하며
print(tot)
```

**Solution3.2**

```python
number = int(input())

s = 0 # 합
for i in range(1, number+1): #1부터 number 까지
    s = s+i # 합에 i를 더함
print(s)
```

