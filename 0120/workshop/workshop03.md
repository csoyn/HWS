# Workshop03

> 함수



### 1. List 의 합 구하기

정수로만 이루어진 list 를 전달 받아 해당 list 의 모든 요소들의 합을 반환하는 list_sum 함수를 built in 함수인 sum() 함수를 사용하지 않고 작성하시오

**Solution1**

```python
def sum_list(*args):
    s = 0 
    for i in args:
        s = s + i
    return s
sum_list(1, 2, 3, 4, 5)
```



###  2. Dictionary 로 이루어진 List 의 합 구하기

Dictionary로 이루어진 list 를 전달 받아 모든 dictionary 의 'age' key 에 해당하는 value들의 합을 반환하는 dict_list_sum 함수를 built in 함수인 sum() 함수를 사용하지 않고 작성하시오

**Solution2**

```python
def dict_list_sum(a, s = 0):
    for i in range(len(a)):
        s = s + a[i]['age']
    return s
```



### 3.  2 차원 List 의 전체 합 구하기
정수로만 이루어진 2 차원 list 를 전달 받아 해당 list 의 모든 요소들의 합을 반환하는 all_list_sum 함수를 built in 함수인 sum() 함수를 사용하지 않고 작성하시오.

**Solution3**

```python
def sum_list2(*args, s=0):
    for i in args:
        if type(i)== list:
            s += sum_list2(i)
        else:
            s += i
    return s
```

