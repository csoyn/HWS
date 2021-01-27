# Workshop05



### 1. 평균 점수 구하기

key 값으로 과목명 , value 값으로 점수를 가지는 dictionary 를 전달 받아 , 전체 과목의 평균 점수를 반환하는 함수 get_dict_avg 함수를 작성하시오.

```python
def get_dict_avg(score_dict):
    return sum(score_dict.values()) / len(score_dict.values())

# 실행
dict1 = {
    'p' : 80,
    'a' : 90,
    'd' : 89,
    'w' : 83
}
get_dict_avg(dict1)
```



### 2. 혈액형 분류하기

여러 사람의 혈액형 (A, B, AB, 에 대한 정보가 담긴 list 를 전달 받아 , key 는 혈액형의 종류 , value 는 사람 수인 dictionary 를 반환하는 count_ blood 함수를 작성하시오.

```python
def count_blood(blood_list):
    result = {}
    types = ['A', 'B', 'O', 'AB']     # 혈액형들 list
    for type_b in types:
        result[f'{type_b}'] = blood_list.count(type_b)   # 각 혈액형의 객수를 셈
    return result  
######
count_blood([
    'A', 'B', 'A','O', 'AB', 'AB',
    'O', 'A', 'B','O', 'B', 'AB'
])
```

