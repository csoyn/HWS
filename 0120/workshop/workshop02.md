# Workshop02

> 데이터 & 제어문

### 1. 간단한 N의 약수 (SWEA #1933)

> 입력으로 1개의 정수 N이 주어진다. 정수 N의 약수를 오름차순으로 출력하는 프로그램을 작성하시오.

---

**Solution1**

```python
N = int(input())

# 아래에 코드를 작성하시오.
for i in range(1,N+1): # 1부터 N을 훑는데,
    if N % i == 0: # N을 나눌 수 있는 수만
        print(i,end='')
```



### 2. 중간값 찾기 (SWEA #2063 변형)

> 중간값은 통계 집단의 수치를 크기 순으로 배열 했을 때 전체의 중앙에 위치하는 수치를 뜻한다. 리스트 numbers에 입력된 숫자에서 중간값을 출력하라.

---

**Solution2**

```python
numbers = [
    85, 72, 38, 80, 69, 65, 68, 96, 22, 49, 67,
    51, 61, 63, 87, 66, 24, 80, 83, 71, 60, 64, 
    52, 90, 60, 49, 31, 23, 99, 94, 11, 25, 24
]

# 아래에 코드를 작성하시오.
numbers.sort() 
len_num = len(numbers)# 리스트의 개수(n) 체크

if len_num % 2 == 1: # n이 홀수면
    median_id = int(((len_num+1)/2)) # (n+1)/2 번째
    print(numbers[median_id-1]) # 인덱스는 0부터니까 -1
else :
    median_id1 =  int(len_num/2)  # n/2 번째
    median_id2 =  int(len_num/2) +1 # (n/2) +1 번째
    print((numbers[median_id1-1]+ numbers[median_id2-1])/2) # 인덱스는 0부터니까 -1
```



### 3. 계단 만들기

> 자연수 number를 입력 받아, 아래와 같이 높이가 number인 내려가는 계단을 출력하시오.

---

```
[입력 예시]
4

[출력 예시]
1
1 2
1 2 3
1 2 3 4
```

**Solution3**

```python
number = int(input())

# 아래에 코드를 작성하시오.
for i in range(1, number+1): # 1부터 number 까지 훑음
    for j in range(1,i+1): # 1 / 1,2 / 1,2,3 /... 1부터 number 를 하나씩
        print(j, end=' ') # 프린트
    print() # line by line으로
```

