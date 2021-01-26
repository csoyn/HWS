# Homework06

> 데이터 구조 및 활용 



### 1.  Built in 함수와 메서드

sorted( )와 .sort( ) 의 차이점을 코드의 실행 결과를 활용하여 설명하시오.

```python
AA = [1, 10, 124, 41, 45, 30]
### sorted()
sorted(AA)     # [1, 10, 30, 41, 45, 124]
print(AA)      
# [1, 10, 124, 41, 45, 30] 원본이 바뀌지 않음.

BB = sorted(AA) 
print(BB)	   
# [1, 10, 30, 41, 45, 124] & AA는 원본 그대로 살아있음.

## sort()
AA.sort()
print(AA)
# [1, 10, 30, 41, 45, 124] 원본이 바뀌어 있음
```

► sorted( )는 원본을 훼손시키지 않고, .sort( )는 원본은 바꿈.



### 2. .extend()와 .append()

```python
### extend() 리스트에 iterable 값을 추가함

# (1)
AA = ['김', '이', '박', '최']
AA.extend('csoyn')
print(AA) 					
# ['김', '이', '박', '최', 'c', 's', 'o', 'y', 'n']

# (2)
AA = ['김', '이', '박', '최']
AA.extend(['최서윤'])
print(AA)
# ['김', '이', '박', '최', '최서윤']

# (3)
AA = ['김', '이', '박', '최']
AA.extend('csoyn', 'Tony')
print(AA) 					# 에러 extend() takes exactly one argument (2 given)

# (4)
AA = ['김', '이', '박', '최']
AA.extend(['csoyn', 'Tony'])
print(AA)
# ['김', '이', '박', '최', 'csoyn', 'Tony']
```

```python
# .append( )

# (1) 
AA = ['김', '이', '박', '최']
AA.append('csoyn')
print(AA)
# ['김', '이', '박', '최', 'csoyn'] -> 위에 (1)에서는 안됐지만, 여기선 가능

# (2)
AA = ['김', '이', '박', '최']
AA.append(['csoyn'])
print(AA)
# ['김', '이', '박', '최', ['csoyn']] -> 리스트 형태로 들어감.

# (3)
AA = ['김', '이', '박', '최']
AA.append('csoyn', 'Tony')
print(AA)    # 에러 append() takes exactly one argument (2 given)

# (4)
AA = ['김', '이', '박', '최']
AA.append(['csoyn', 'Tony'])
print(AA)
# ['김', '이', '박', '최', ['csoyn', 'Tony']] -> 리스트 형태로 들어감.
```



### 3. 복사가 잘 된 건가
아래의 코드를 실행 하였을 때 , 변수 a 와 b 에 담긴 list 의 요소가 같은지 혹은 다른지 여부를 판단하고 그 이유를 작성하시오.

```python
a  = [1, 2, 3, 4, 5]
b =  a
a[2] = 5

print(a)   # - > [1, 2, 5, 4,5]
print(b)   # - > [1, 2, 5, 4,5]
```

►  a 와 b 를 print 해본 결과, b는 a의 원본이 아닌 `a[2] = 5` 코드로 변형된 a 리스트와 동일했다.

그 이유는,  `b =  a`는 a가 가르키고 있는 리스트를 b가 그대로 가르키고 있기 때문에, a가 변형되면 b도 같이 변형 된 것이다.