# Workshop

> 데이터 & 제어문

## 1. 세로로 출력하기

> 자연수 number를 입력 받아, 1부터 number까지의 수를 세로로 한줄씩 출력하시오.

---
**Solution1**

```python
number = int(input())
# 아래에 코드를 작성하시오.
A = 0
while A < number : # A가 number에 도달할 때까지
    A = A +1 # A에 1씩 더함
    print(A) 
```



## 2. 거꾸로 세로로 출력하기

> 자연수 number를 입력 받아, number부터 1까지의 수를 세로로 한줄씩 출력하시오.

**Solution2**

```python
number = int(input())

# 아래에 코드를 작성하시오.
A = number
while A > 0: # A가 0에 도달할 때까지
    A = A - 1 # A에 -1씩 
    print(A)
```



## 3. N줄 덧셈 (SWEA #2025)

> 입력으로 자연수 number가 주어질 때, 1부터 주어진 자연수 number까지를 모두 더한 값을 출력하시오. 단, 주어지는 숫자는 10000을 넘지 않는다. 예를 들어, 주어진 숫자가 10일 경우 1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9 + 10 = 55이므로, 출력해야 할 값은 55이다.

---
**Solution3**

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

