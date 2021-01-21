# Homework03

> 함수

[toc]



### 1.Built in 함수

> Python에서 기본으로 사용할 수 있는 built in 함수를 최소 5 가지 이상 작성하시오



**Solution1**

print( ) , type( ),  int( ), str( ), float( ), min( ), max( ), round( ),  len( )... 



### 2. 정중앙 문자

문자열을 전달 받아 해당 문자열의 정중앙 문자를 반환하는 get_middle_char 함수를 작성하시오 .

 단 , 문자열의 길이가 짝수일 경우에는 정중앙 문자 2 개를 반환한다.

**Solution2**

```python
def get_middle_char(char):
    len_char = len(char) # 문자열 길이(n) 체크
    
    if len(char) % 2 ==1:
        middle_id = (len_char+1)/2 # 홀수인 경우 n+1/2 번째 
        print(char[int(middle_id-1)]) # 인덱스는 0부터 시작이니까 -1 
    else :
        middle_id1 = (len_char)/2 # 짝수인 경우 n/2 번째 
        middle_id2 = ((len_char)/2)+1 # 짝수인 경우 (n/2)+1 번째
        print(char[int(middle_id1-1)], char[int(middle_id2-1)]) #인덱스는 0부터시작이니까 -1
```



###  3. 위치 인자와 키워드 인자

다음과 같이 함수가 선언되어 있을 때 , 보기 (1)~(4) 중에서 실행 시 오류가 발생하는 코드를 고르시오

![image-20210120205939527](homework03.assets/image-20210120205939527-1611144522858.png)

**Solution3**

(4) 번

위치인자의 순서 때문

' `길동`의 지역은  ` 구미` 입니다. '를 출력하기 위해서는 아래처럼 입력해야한다.

```python
ssafy(name='길동',location ='구미') # 가능
ssafy('길동',location ='구미') # 가능
ssafy('길동','구미') # 가능
ssafy('구미','길동') # 얘는 구미의 지역는 길동입니다.
```



### 4. 나의 반환값은
다음과 같이 함수를 선언하고 호출하였을 때 , 변수 result 에 저장된 값을 작성하시오

![image-20210120210908431](homework03.assets/image-20210120210908431.png)

**Solution4**

함수의 결과값은 10이나, result에는 None(Nonetype)



### 5. 가변 인자 리스트

가변인자 리스트를 사용하여 , 갯수가 정해지지 않은 여러 정수들을 전달 받아 해당 정수들의 평균 값을 반환하는 my_avg 함수를 작성하시오.

**Solution5**

```python
def my_avg(*args):
    avg = sum(args) / len(args)
    return avg  
```







