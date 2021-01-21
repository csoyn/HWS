# Practice01

> 함수



### 1. `abs()` 직접 구현하기

> 절댓값은 숫자형 자료(int, float)가 들어오면 절댓값을 반환하고, 복소수형 자료(complex)가 들어오면 해당하는 자료의 크기를 반환합니다. 파이썬 내장 함수 `abs()`를 직접 구현한 `my_abs()`를 작성하시오.

**Solution1**

```python
def my_abs(x):
    if type(x) == float or type(x) == int :
        if x>0:
            return x
        elif x == -0.0 or x == +0.0 or x == 0.0 :
            x=0
            return x
        else:
            return -x
    elif type(x) == complex:
            return ((x.real)**2 + (x.imag)**2 )**0.5
    else:
        pass
    
    
print(my_abs(3+4j))
print(my_abs(-0.0))
print(my_abs(-5))
print(abs(3+4j), abs(-0.0), abs(-5))
print(my_abs(+0.0))

print(my_abs(0.0))
```



### 2. `all()` 직접 구현하기

> `all()`은 인자로 받는 iterable(range, list)의 모든 요소가 참이거나 비어있으면 True를 반환합니다. 
>
> 파이썬 내장 함수 `all()`을 직접 구현한 `my_all()`을 작성하시오.

**Solution2**

```python
def my_all(elemets):
    for e in elemets:
        if not e:
            return False
        else:
             return True       
    return True

print(my_all([]))
print(my_all([1, 2, 5, '6']))
print(my_all([[], 2, 5, '6']))

print(all([]), all([1, 2, 5, '6']), all([[], 2, 5, '6']))
```



### 3.  `any()` 직접 구현하기

> `any()`는 인자로 받는 iterable(range, list)의 요소 중 하나라도 참이면 True를 반환하고, 비어있으면 False를 반환합니다. 
>
> 파이썬 내장 함수 `any()`을 직접 구현한 `my_any()` 함수를 작성하시오.

**Solution3**

```python
def my_any(elemets):
    for e in elemets:
        if e:
            return True
    return False

print(my_any([1, 2, 5, '6']))
print(my_any([[], 2, 5, '6']))
print(my_any([0]))
print(any([1, 2, 5, '6']), any([[], 2, 5, '6']), any([0]))
```

