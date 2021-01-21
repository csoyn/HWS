# Practice 2

> 함수



### 1. 불쌍한 달팽이

> 달팽이는 낮 시간 동안에 기둥을 올라간다. 하지만 밤에는 잠을 자면서 어느 정도의 거리만큼 미끄러진다. (낮 시간 동안 올라간 거리보다는 적게 미끄러진다.)
>
> 달팽이가 기둥의 꼭대기에 도달하는 날까지 걸리는 시간을 반환하는 함수 `snail()`을 작성하시오.

> 함수의 인자는 다음과 같다.
1. 기둥의 높이(미터)
2. 낮 시간 동안 달팽이가 올라가는 거리(미터)
3. 달팽이가 야간에 잠을 자는 동안 미끄러지는 거리(미터)

**Solution1**

```python
def snail(height, day, night, time=0):
    moved = day-night #3
    will_move = height-moved  # 100-3 =97
    
    if will_move % moved ==0: # 100에  도달했으면
        time = will_move // moved # 이만큼 걸림
    else: # 모질라면
        time = will_move // moved +1 #97//3+1 (32+1)
        return time
    
 print(snail(100, 5, 2))   
```



###  2. 자릿수 더하기 (SWEA #2058)

> 자연수 number를 입력 받아, 각 자릿수의 합을 계산하여 출력하시오.

**Solution2**

```python
def sum_of_digit(number, s=0):
    for i in str(number): 
        s += int(i) 
    return s

print(sum_of_digit(1234))
print(sum_of_digit(4321))
```

