# Practice 01

> 데이터 & 제어문

[toc]



### 1.  갯수 구하기

> 주어진 리스트의 요소는 학생 이름으로 구성되어 있다. 학생들의 수를 출력하시오.

---

**Solution1**

```python
students = ['김철수', '이영희', '조민지']

# 아래에 코드를 작성하시오.
stu_cnt = len(students) # 3
print(f'학생은 총{student}명 입니다.') #학생은 총 3명 입니다
```



### 2.  득표수 구하기

> 주어진 리스트는 반장 선거 투표 결과이다. 이영희의 총 득표수를 출력하시오.

**Solution2**

```python
students = ['이영희', '김철수', '이영희', '조민지', '김철수', '조민지', '이영희', '이영희']

cnt = 0
for i in students :
    if i == '이영희':
        cnt+=1
print(f'이영희의 총 득표수는 {cnt}입니다.')   #이영희의 총 득표수는 4입니다.
```



### 3. 최댓값 구하기

> 주어진 리스트의 요소 중에서 최댓값을 출력하시오.

**Solution3**

```python
numbers = [7, 10, 22, 4, 3, 17]

# 아래에 코드를 작성하시오.
max(numbers) # 22
```



###  4. 최솟값 구하기

> 주어진 리스트의 요소 중에서 최솟값을 출력하시오.

```python
numbers = [7, 10, 22, 4, 3, 17]

# 아래에 코드를 작성하시오.
min(numbers) # 3
```



### 5.  최댓값과 등장 횟수 구하기

> 주어진 리스트의 요소 중에서 최댓값과 등장 횟수를 출력하시오.

**Solution5**

```python
numbers = [7, 10, 22, 7, 22, 22]

# 아래에 코드를 작성하시오.
max_num = max(numbers)
max_cnt = 0
for i in numbers :
    if i == max_num:
        max_cnt +=1
print(f'최댓값{max_num}는 총{max_cnt}번 등장합니다.') # 최댓값22는 총3번 등장합니다.
```



###  6. 5의 개수 구하기

> 주어진 리스트의 요소 중에서 5의 개수를 출력하시오.

**Solution6**

```python
numbers = [7, 17, 10, 5, 4, 3, 17, 5, 2, 5]

# 아래에 코드를 작성하시오.
cnt = 0
for i in numbers :
    if i ==5:
        cnt+=1
print(f'5는 총 {cnt}개입니다.')    # 5는 총 3개입니다.
```



### 7. 'a'가 싫어


> 입력으로 짧은 영단어 word가 주어질 때, 해당 단어에서 'a'를 모두 제거한 결과를 출력하시오.

**Solution7**

```python
word = input()

# 아래에 코드를 작성하시오.
for i in word:
    if i != 'a': # a가 아닌 애들만
        print(i, end='')
```



### 8. 단어 뒤집기

> 입력으로 짧은 영어단어 word가 주어질 때, 해당 단어를 역순으로 뒤집은 결과를 출력하시오.

**Solution8**

```python
word = input()

# 아래에 코드를 작성하시오.
new_word = word[::-1] # 거꾸로 하나씩
print(new_word)
```

