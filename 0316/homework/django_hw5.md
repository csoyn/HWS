# Django hw05

> Django Model form View structure



### Problem

아래 작성된 views.py의 코드 일부를 보고 문제에 알맞은 답을 서술 하시오.

```python
def create(request):
    """
    GET : 새 게시글을 작성하는 탬플릿을 랜더
    POST : DB에 새 게시글 정보 저장(생성)
    """
    if request.method == 'POST':
        # request.POST 정보가 들어가있는 form 인스턴스를 생성
        form = ArticleForm(request.POST)
        # 유효성 검사
        if form.is_valid():
            # 검사를 통과하면 저장
            article = form.save()
            return redirect('articles:detail', article.pk)
    else:
        # ModelForm Class로 form 인스턴스를 생성
        form = ArticleForm()

    # 탬플릿을 랜더 (유효성 검사를 통과하지 못한 경우)
    # 유효성 검사에서 사용한 form 인스턴스를 재사용하기 때문에
    # 유효성 검사를 통과하지 못했을때 기존 내용을 보존할 수 있다!
    context = {
        'form': form
    }
    return render(request, 'articles/create.html', context)

```

#### 1. 왜 변수 context는 if else 구문과 동일한 레벨에 작성 되어있는가?

**답)**  `context`에 있는 form은 `request.POST`의 정보가 들어가 있는 form 인스턴스이고,

 검사를 통과했다면 DB에 저장이 되고, 유효성 검사를 통과하지 못했을 때는 유효성검사에서 사용한 form 인스턴스를 재사용하기 때문에 기존 내용을 보존할 수 있기 때문에

( 유효성 검사를 통과하지 못한 경우,내용을 삭제하지 않음 & 유효성 검사를 통과하지 못한 부분만 삭제)

#### 2. 왜 request의 http method는 POST 먼저 확인하도록 작성하는가?

**답)** POST만 허용하기 위해서(DB에 create), 나머지 방식들은 템플릿을 다시 보여주는 형식으로 처리하기 위해서

(참고 https://docs.djangoproject.com/en/3.1/topics/forms/#the-view )