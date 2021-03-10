# Django hw03

> Django Model



### 1. Model반영하기

“Django가 Model 에 생긴 변화를 DB 에 반영하는 방법'' 을 뜻하는 용어를 작성하시오.

**답)** Migration



### 2.  Model 변경사항 저장하기
<img src="django_hw3.assets/image-20210310210704528.png" alt="image-20210310210704528" style="zoom:67%;" />

위에서 작성한 Model 의 변경 사항을 저장하기 위한 명령어를 작성하시오 . 이로 인해 생성된 파일에 대응되는 SQL 문을 확인하는 명령어와 출력 결과를 작성하시오.

**답)** python manage.py makemigrations / sqlmigrate 



### 3. Python Shell
Django에서 사용 가능한 모듈 및 메서드를 대화식 Python Shell 에서 사용하려고 할 때 , 어떠한 명령어를 통해 해당 Shell 을 실행할 수 있는지 작성하시오.

**답)** python manage.py shell_plus



### 4. Django Model Field
Django에서 Model 을 정의할 때 사용할 수 있는 필드 타입을 5 가지 이상 작성하시오.

**답)** IntegerField / CharField / TextField / DateTimeField / AutoField