# Django_workshop05

> Django Model Form



### Problem

아래의 코드들을 참고하여 각 문항에 답하시오.

```python
# models.py
class Reservation(models.Model):
    name = models.CharField(max_length = 10)
    date = models.DateField()
```

#### 1) 모델 폼을 정의

```python
# forms.py
from django import forms
from .models import Reservation

class Reservation(forms.ModelForm): # a
    # Model과 연결 
    class Meta: # b
        model = Reservation
        fields = '__all__'
```

**답)**  (a) - forms.ModelForm / (b)- Meta



#### 2) CREATE 오류 발생- 이유&해결방법

```python
def create(request):
    if request.method =='POST':
        form = ReservationForm(request.POST)
        # 유효성 검사
        if form.is_valid():
            Reservation = form.save()
            return redirect('reservations:detial' , reservation.pk )
       # return redirect('reservations:create')
    else:
        form = ReservationForm()

        context = {
            'form': form
        }
        return render(request, 'reservations/create.html', context)
```

**답)** form이 유효하지 않은 경우에 문제가 발생(주석처리한 부분이 필요 ) / context 부터 쉬프트 탭 : form 이 재사용할 수 있다.



#### 3) UPDATE 

```python
def update(request, pk):
    reservation = Reservation.objects.get(pk=pk)

    if request.method == 'POST':
        # POST : DB 특정 게시글 정보 수정
        # ModelForm 클래스로 인스턴스를 생성!
        form = ReservationForm(request.POST, instance=reservation) # a

        if form.is_valid():
            reservation = form.save()
            return redirect('reservations:detail', reservation.pk)
    else:
        form = ReservationForm(instance=article) # b

    context = {
        'form': form
    }
    return render(request, 'articles/edit.html', context)
```



**답)**  (a) :  form = ReservationForm(request.POST, instance=reservation)

​       (b)  form = ReservationForm(instance=article)



#### 4) Edit

```html
<form method="POST">
  {% csrf_token %}
  {{ form.(a) }} 
</form>
```



**답)** form.as_p /  form.as_table /   form.as_ul

 