# Workshop06



### 1.  무엇이 중복일까

```python
def duplicated_letters(word):
    result = [alpha for alpha in word if word.count(alpha) >=2]
    return list(set(result))
print(duplicated_letters('apple'))
print(duplicated_letters('banana'))
```



### 2. 소대소대 

```python
def low_and_up(word):
    new_word = ''
    for idx, alpha in enumerate(word):
        if idx % 2:
            new_word += alpha.upper()
        else:
            new_word += alpha.lower()
    return new_word


print(low_and_up('apple'))
print(low_and_up('banana'))
```



### 3. 숫자의 의미

```python
# 새로운 list를 만들고 순서대로, 다음 인덱스와 중복되었는지 안되었는지 검사해서
# append를 하려고 했는데 잘 안돼서 휴
```

