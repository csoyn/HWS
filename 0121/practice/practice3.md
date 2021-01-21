# Practice 3

> 자료 구조 



###  회문 판별

> 회문 또는 팰린드롬은 거꾸로 읽어도 제대로 읽는 것과 같은 문장이나 낱말, 숫자, 문자열 등을 말한다. 
>
> 입력으로 짧은 영어단어 word가 주어질 때, 해당 단어가 회문이면 True 회문이 아니면 False를 반환하는 함수를 작성하시오.
>
> 이때, 반복문(`while`)과 재귀 함수를 사용해서 각각 작성하시오.



```python
# ㅠㅠㅠㅠㅠㅠㅠ
def is_pal(word):
    if list(word) == list(word)[::-1]:
        return True
    else :
        return False

is_pal('tomato') #=> False
is_pal('racecar') #=> True
is_pal('azza') #=> True
```

