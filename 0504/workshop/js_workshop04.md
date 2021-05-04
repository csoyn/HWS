# JS_Workshop04

>AJAX  요청에 대한 이해



### Django Django 프로젝트에서 게시글 좋아요 기능을 axios 라이브러리를 활용하여 AJAX 요청으로 구현하시오 .
• 로그인 사용자의 “좋아요 ” 여부에 따라 아이콘이 변경되어야 한다 .
• 변경된 총 “좋아요 ”를 누른 사용자의 수가 반영되어야 한다 .
• 위의 모든 요구 사항은 페이지의 새로 고침 없이 진행되어야 한다 .

```html
{% extends 'base.html' %}

{% block content %}
  <h1>Articles</h1>
  {% if request.user.is_authenticated %}
    <a href="{% url 'articles:create' %}">[CREATE]</a>
  {% else %}
    <a href="{% url 'accounts:login' %}">[새 글을 작성하려면 로그인하세요.]</a>
  {% endif %}
  <hr>
  {% for article in articles %}
    <p>
      <b>작성자 : <a href="{% url 'accounts:profile' article.user.username %}">{{ article.user }}</a></b>
    </p>
    <p>글 번호 : {{ article.pk }}</p>
    <p>글 제목 : {{ article.title }}</p>
    <p>글 내용 : {{ article.content }}</p>
    <div>
      <form class="like-form" data-article-id="{{ article.pk }}">
        {% csrf_token %}
        {% if request.user in article.like_users.all %}
          <button class="btn btn-link text-danger">
            <i class="like-{{ article.pk }} fas fa-heart"></i>
          </button>
        {% else %}
          <button class="btn btn-link text-danger">
            <i class="like-{{ article.pk }} far fa-heart"></i>
          </button>
        {% endif %}
      </form>
    </div>
    <p>
      <span class="count-{{ article.pk }}">{{ article.like_users.all|length }}</span>
      명이 이 글을 좋아합니다.
    </p>
    <a href="{% url 'articles:detail' article.pk %}">[DETAIL]</a>
    <hr>
  {% endfor %}
  <!-- axios -->
  <script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>

  <script>
    const forms = document.querySelectorAll('.like-form')
     // console.log(forms)   Nodelist
     // CSRF 꺼냄 
    const csrftoken = document.querySelector('[name=csrfmiddlewaretoken]').value
    forms.forEach( form => {
      // console.log(form)   form element
      form.addEventListener('submit' , function (event) {
        // submit event 막기
        event.preventDefault()
        // console.log(event)
        // 요청 : 좋아요 -> 좋아요 취소 / 좋아요 취소 -> 좋아요
        // article_pk 필요함 -> HTML data attribute
        console.log(event.target.dataset)

        console.log(event.target.dataset.articleId)
        const articleId = event.target.dataset.articleId
        // article_pk있음 -> 해당 게시물 좋아요, 취소 요청
        // 403 !! -> Forbidden (CSRF 검증 실패)
        // CSRF 가져옴
        // const csrftoken = document.querySelector('[name=csrfmiddlewaretoken]').value
        // CSRF가 동일하니까 for 문 바깥으로 꺼내자
        
        // CSRF를 어디에 담아서 보내야하다  https://github.com/axios/axios
        // 
        // axios.post(`http://127.0.0.1:8000/articles/${articleId}/likes`)

        // Send a POST request
          axios({
            method: 'post',
            baseURL: 'http://127.0.0.1:8000/articles/',
            url: `${articleId}/likes/`,
            headers: {
              'X-CSRFToken': csrftoken
          }
        })
        .then(response => {
            // console.log(response)
            const liked = response.data.liked
            const likeIcon = document.querySelector(`.like-${articleId}`)
            if (liked) {
              likeIcon.classList.remove('far')
              likeIcon.classList.add('fas')
            } else {
              likeIcon.classList.remove('fas')
              likeIcon.classList.add('far')
            }

            const count = response.data.count
            const countSpan = document.querySelector(`.count-${articleId}`)
            countSpan.innerText = count
          })
      })
    })
  </script>
{% endblock %}
```

```python
# articles/views.py
@require_POST
def likes(request, article_pk):
    if request.user.is_authenticated:
        article = get_object_or_404(Article, pk=article_pk)

        if article.like_users.filter(pk=request.user.pk).exists():
        # if request.user in article.like_users.all():
            # 좋아요 취소
            article.like_users.remove(request.user)
            liked = False
        else:
            # 좋아요 누름
            article.like_users.add(request.user)
            liked = True
    
        like_status = {
            'liked' : liked,
            'count' : article.like_users.count()
        }
    return JsonResponse(like_status)

```

