# SQL



### 1. SQL 용어 및 개념
1) **스키마** : 관계형 데이터베이스에서 구조와 제약조건에 관련한 전반적인 명세를 기술 한 것
2) **테이블** : 열과 행의 모델을 사용해 조직된 데이터 요소들의 집합 
3) **레코드**:고유한 데이터 형식이 지정되는 열
4) **컬럼**: 단일 구조 데이터 항목을 가리키는 행
5) **기본키** 각 행의 고유값



### 2. SQL 문법

DML(Data Manipulation Language) :  문장의 첫 단어로 표시하는 기능

**SELECT /  INSERT /  UPDATE / DELETE**

(1) CREATE는 아님.



### 3. Relational DBMS
RDBMS(**관계형 데이터베이스**)의 개념적 정의와 이를 기반으로 한 DB Engine 의 종류 세가지 이상 작성하시오

**RDB** : 키(key)와 값(value)들의 간단한 관계를 테이블화 시킨 매우 간단한 원칙의 전산정보 데이터베이스

& 데이터 [관계형 모델](https://ko.wikipedia.org/wiki/관계형_모델)에 기초하는 DB

**RDBMS** : RDB 관리를 위한 소프트웨어 / Oracle , MS Accesss, MySQL



### 4. INSERT INTO

다음과 같은 스키마를 가지는 테이블이 있을 때, 아래의 보기 (1) ~ (4) 중 틀린 문장을 고르시오.

```sql
CREATE TABLE classmate(
	name TEXT,
	age INT,
	address TEXT
);
```

```sql
/* (1) */ INSERT INTO classmates (name, age, address)
VALUES(‘홍길동’, 20, ‘seoul’);

/* (2) */ INSERT INTO classmates VALUES(‘홍길동’, 20, ‘seoul’);

/* (3) */ insert into classmates
values(address=‘seoul’, age=20, name=‘홍길동’);

/* (4) */ insert into classmate (address, age, name)
values(‘seoul’, 20, ‘홍길동’);
```

(4)번 ...?



### 5. 와일드카드 문자

SQL에서 사용가능한 와일드카드 문자인 %와 _을 비교하여 작성하시오.

- % : 문자길이 상관 없음.
- _ : 한 글자

```sql
SELECT * FROM TABLE_A WHERE NAME LIKE '%라면'
SELECT * FROM TABLE_A WHERE NAME LIKE '_라면'
```





