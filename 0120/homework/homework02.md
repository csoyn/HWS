# Homework02

> 데이터 & 제어문

### 1. mutable & immutable

제시 된 컨테이너들을 각각, 변경 가능한 것(mutable)과 변경 불가능한 것(immutable)으로 분류하시오.

> String, List, Tuple, Range, Set, Dictionary

**Solution1**

- `tuple` `range` `set` : 수정 불가능한 immutable

- `string` `list` `dict` : 수정 가능한 mutable



### 2. 홀수 list

range와 slicing을 활용하여 1부터 50까지 숫자 중 홀수로 이루어진 리스트를 만드시오.

**Solution2**

```python
list1 = list(range(1,51)) # 1 부터 50까지
odd_list1 = list1[0::2] # 1(인덱스0) 부터 끝까지 2씩 증가시킴
print(odd_list1)
```



### 3. dictionary 생성

반 학생들의 정보를 이용하여 key는 이름, value는 나이인 dictionary를 만드시오.

**Solution3**

```python
# 아래에 코드를 작성하시오.
dict_info = {'김싸피':'28', '이싸피':'25', '박싸피':'26', '최싸피':'27','Tony':'29'} 
```



### 4. 반복문으로 네모 출력

두 개의 정수 n과 m이 주어졌을 때, 가로의 길이가 n, 세로의 길이가 m인 직사각형 형태를 별(*) 문자를 이용하여 출력하시오. 단, 반복문을 사용하여 작성하시오.

**Solution4**

```python
n = 5
m = 9

# 아래에 코드를 작성하시오.
for i in range(m): # 세로 9만큼
    for j in range(n): #  가로 *5개
        print('*', end='') # 프린트하는데
    print()  #4. line by line 프린트
```



### 5. 조건 표현식

제시된 if 문을 조건 표현식으로 바꾸어 작성하시오.
```python
temp = 36.5
if temp >= 37.5:
    print('입실 불가')
else:
    print('입실 가능')
```

**Solution5**

조건표현식  : `true_value if <조건식> else false_value` 

```python
temp = 36.5

# 아래에 코드를 작성하시오.
print('입실 불가') if temp >= 37.5 else print('입실 가능')
```



### 6. list 평균값

제시된 list의 평균 값을 출력하시오. `scores = [80, 89, 99, 83]` 

**Solution6**

```python
print(sum(scores) / len(scores))
```







 