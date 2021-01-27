# Pratice1 (01.26)

> 복잡한 자료구조의 (2차원리스트) 반복문



### 1. 복잡한 리스트의 합

**Solution1.1**

```python
#  for 문을 활용하여 풀이하기

def sum_list(numbers):
    sum_nums = []
    for num_list in numbers:    # for element in list:
        sum_nums.append(sum(num_list))
    return sum(sum_nums)
print(sum_list([[1, 4], [10, 5], [20, 30]]))
```

**Solution1.2**

```python
# Index로 접근하여 풀이하기

def sum_list_index(numbers, result = 0):
    for element in range(0, len(numbers)): #  0
            result += sum(numbers[element])
    return result
print(sum_list_index([[1, 4], [10, 5], [20, 30]]))
```

**Solution1.3**

```python
# while 문을 활용하여 풀이하기

def sum_list_while(numbers, result = 0):
    idx = 0
    while idx < len(numbers):
        result += sum(numbers[idx])
        idx +=1
    return result  
print(sum_list_while([[1, 4], [10, 5], [20, 30]]))
```



### 2. 시험 점수

**Solution2.1**

```python
# 학생별 출력
for stu_list in students:    
    sum_score = 0
    for score in stu_list:
        sum_score +=score
    print(sum_score, end='\n')
```

**Solution2.2**

```python
# 과목별 출력
for idx1 in range(0,len(students)):
    sum_sub = 0
    for idx2 in range(0,len(students[0])):
        sum_sub +=students[idx2][idx1]
    print(sum_sub, end='\n')
```

